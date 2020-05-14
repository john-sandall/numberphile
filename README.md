# Numberphile

[![ben sparks](./images/2020-03-20_ben_sparks.jpg)](https://www.youtube.com/watch?v=k6nLfCbAzgo)

<div align="center"><a href="https://www.youtube.com/watch?v=k6nLfCbAzgo" style="font-size: large;"><strong>Watch <em>The Coronavirus Curve - Numberphile</em> on YouTube</strong></a></div>

**Video Description**
> _Ben Sparks explains (and codes) the so-called SIR Model being used to predict the spread of cornavirus (COVID-19)._
> 
> **LINKS**
> - National Health Service (UK) advice on Coronavirus: https://www.nhs.uk/conditions/coronavirus-covid-19/
> - Ben Sparks: https://www.bensparks.co.uk
> - Use the Geogebra file Ben created for this video: https://www.geogebra.org/m/nbjfjtpv
> - Another good file courtesy of Juan Carlos Ponce Campuzano: https://www.geogebra.org/m/utbemrca 
> - Washington Post simulator: https://www.washingtonpost.com/graphics/2020/world/corona-simulator/
> - Extended presentation by Nick Jewell for MSRI: https://youtu.be/MZ957qhzcjI
> - More videos with Ben Sparks: http://bit.ly/Sparks_Playlist
> 
> **SOME OTHER YOUTUBERS ON THIS TOPIC...**
> - 3blue1brown on the exponential growth of epidemics: https://youtu.be/Kas0tIxDvrg
> - Tom Crawford on the SIR Model: https://youtu.be/NKMHhm2Zbkw
> - Kurzgesagt on COVID-19: https://youtu.be/BtN-goy9VOY
> 
> **NUMBERPHILE**
> - Website: http://www.numberphile.com/
> - Numberphile on Facebook: http://www.facebook.com/numberphile
> - Numberphile tweets: https://twitter.com/numberphile
> Subscribe: http://bit.ly/Numberphile_Sub
> 
> Videos by [Brady Haran](https://www.bradyharanblog.com/) ([@BradyHaran](https://twitter.com/BradyHaran))


# Tips & Tricks
```
# Activate environment
workon numberphile

# Update packages from requirements.txt
pip-sync
 
# Install new package & update requirements.txt
pip install new-package-name
pip freeze  # to check version number

# copy paste package & version to requirements.in
pip-compile requirements.in
pip-sync
```

# Setup
```
# Install virtualenv
pip install virtualenv


# Install virtualenvwrapper (http://virtualenvwrapper.readthedocs.org/en/latest/index.html)
pip install virtualenvwrapper
# Tell shell to source virtualenvwrapper.sh and where to put the virtualenvs by adding following to .zshrc
zshconfig
#    # "Tell shell to source virtualenvwrapper.sh and where to put the virtualenvs"
#    export WORKON_HOME=$HOME/.virtualenvs
#    export PROJECT_HOME=$HOME/code
#    source /usr/local/bin/virtualenvwrapper.sh
source ~/.zshrc
source /usr/local/bin/virtualenvwrapper.sh
# Now let's make a virtualenv
mkvirtualenv venv
workon venv
# Commands `workon venv`, `deactivate`, `lsvirtualenv` and `rmvirtualenv` are useful
# WARNING: When you brew install formulae that provide Python bindings, you should not be in an active virtual environment.
# (https://github.com/Homebrew/homebrew/blob/master/share/doc/homebrew/Homebrew-and-Python.md)
deactivate


# Create virtualenv & install packasges
mkvirtualenv numberphile
pip install pip-tools
pip-sync
python -m ipykernel install --user --name numberphile --display-name "Python (numberphile)"

# Install Jupyter extensions JS/CSS & enable required extensions
jupyter contrib nbextension install
jupyter nbextension enable toc2/main

# Initialise nbinteract & create .html
nbinteract init
nbinteract notebooks/The_Coronavirus_Curve.ipynb
```
