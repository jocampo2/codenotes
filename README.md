# My list of frequently used code 

...So I don't have to look it up everytime

## Reload modules in notebook
```
%load_ext autoreload
%autoreload 2
```

## Bash for loop zero pad
```
for i in $(seq -f "%05g" 10 15)
do
  echo $i
done
```

## Import from parent dir
```
import sys
sys.path.insert(0,'..')
```

## Use specific gpu
```
import tensorflow as tf
gpus = tf.config.list_physical_devices('GPU')
tf.config.experimental.set_visible_devices(gpus[1], 'GPU')
tf.config.list_physical_devices('GPU')
```

## Colorbar size to match fig
```
implot = ax.imshow(psi1,cmap="jet")
im_ratio = psi1.shape[0]/psi1.shape[1]
plt.colorbar(implot,fraction=0.046*im_ratio, pad=0.04)
```

## Best savefig options
```
plt.savefig(bbox_inches='tight',facecolor='white', transparent=False)
```

## Plt fonts
```
plt.rcParams['font.family'] = 'STIXGeneral'
plt.rcParams.update({'font.size': 14})

from matplotlib import rc
rc('font', **{'family': 'serif', 'serif': ['Computer Modern']})
rc('text', usetex=True)
```

## Legend options
```
ax1.legend(loc='upper center', bbox_to_anchor=(0.5, 1.4),frameon=False)
plt.ylabel(labelpad=10)
```

## Instal tensorflow mac M1 chip
https://developer.apple.com/metal/tensorflow-plugin/

## Set cpu
```
import os
os.environ['CUDA_VISIBLE_DEVICES'] = '-1'
```

## Elastic beanstalk output locations
```
/var/app/current/ - location of files
/var/log/web.stdout.log - output of website clicks
```

## remove powerpoint image border chrome view
save as pdf