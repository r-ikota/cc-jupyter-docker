Setting a number format
#######################

IPython
--------

    >>> import numpy as np
    >>> % precision 3
    '%.3f'
    >>> a = 3.524353
    >>> a
    3.524

Pandas
------


    >>> import numpy as np, pandas as pd
    >>> def float_formatter(x):
    ...     if np.isnan(x):
    ...         return ""
    ...     else:
    ...         return "{0:0.3f}".format(x)
    >>> df = pd.DataFrame({'a': [1.234567, -3.456789], 'b': [-2.333333, 5.22222222]})
    >>> df.to_csv(float_format=float_formatter)
    ',a,b\n0,1.235,-2.333\n1,-3.457,5.222\n'

    >>> import numpy as np, pandas as pd
    >>> pd.options.display.float_format = '{:.2f}'.format
    >>> df = pd.DataFrame({'a': [1.234567, -3.456789], 'b': [-2.333333, 5.22222222]})
    >>> df.describe()
            a     b
    count  2.00  2.00
    mean  -1.11  1.44
    std    3.32  5.34
    min   -3.46 -2.33
    25%   -2.28 -0.44
    50%   -1.11  1.44
    75%    0.06  3.33
    max    1.23  5.22    

In a Jupyter notebook, type the following:    

    >>> import numpy as np, pandas as pd
    >>> df = pd.DataFrame({'a': [1.234567, -3.456789], 'b': [-2.333333, 5.22222222]})
    >>> df.style.format('{:.2f}')

matplotlib
------------


.. code-block:: python

    import numpy as np
    import matplotlib.pyplot as plt
    x = np.linspace(0., 1., 21)
    y = 1.0e-5*np.sin(2.0*np.pi*x)
    plt.plot(x,y)
    plt.ticklabel_format(scilimits=(0,0))