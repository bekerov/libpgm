linear gaussian bayesian network
================================

This is an example input file for a Bayesian network with linear Gaussian conditional probability distributions. It provides linear Gaussian CPD data for the same graph skeleton as in the :doc:`discrete case <unittestdict>`::

    {
        "Vdata": {
            "Grade": {
                "mean_base": 80, 
                "mean_scal": [
                    -0.25, 
                    0.25
                ], 
                "parents": [
                    "Difficulty", 
                    "Intelligence"
                ], 
                "variance": 5, 
                "type": "lg", 
                "children": [
                    "Letter"
                ]
            }, 
            "Intelligence": {
                "mean_base": 50, 
                "mean_scal": [], 
                "parents": null, 
                "variance": 18, 
                "type": "lg", 
                "children": [
                    "SAT", 
                    "Grade"
                ]
            }, 
            "Difficulty": {
                "mean_base": 50, 
                "mean_scal": [], 
                "parents": null, 
                "variance": 18, 
                "type": "lg", 
                "children": [
                    "Grade"
                ]
            }, 
            "Letter": {
                "mean_base": -110, 
                "mean_scal": [
                    2
                ], 
                "parents": [
                    "Grade"
                ], 
                "variance": 10, 
                "type": "lg", 
                "children": null
            }, 
            "SAT": {
                "mean_base": 10, 
                "mean_scal": [
                    1
                ], 
                "parents": [
                    "Intelligence"
                ], 
                "variance": 10, 
                "type": "lg", 
                "children": null
            }
        }
    }
