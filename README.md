Test
====
sdfksdflkjsldfj
sdlfkjlfjslkjdf
1
2
4
55

3
;re

we34


345345


34545

import androidx.lifecycle.LiveData
import androidx.lifecycle.MutableLiveData
import androidx.lifecycle.ViewModel
import androidx.lifecycle.ViewModelProvider

// Override ViewModelProvider.NewInstanceFactory to create the ViewModel (VM).
class SignInViewModelFactory(private val repository: NoteRepository) :
    ViewModelProvider.NewInstanceFactory() {
    override fun <T : ViewModel?> create(modelClass: Class<T>): T = SignInViewModel(repository) as T
}


class SignInViewModel(val repository: NoteRepository) : ViewModel() {


    private val _isLoading = MutableLiveData(true)

    val emailText = MutableLiveData("")
    val passwordText = MutableLiveData("")


    val isLoading: LiveData<Boolean> = _isLoading



