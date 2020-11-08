---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277548"
---
# Az. ResourceMover modülü
## Tanım
Microsoft Azure PowerShell: ResourceMover cmdlet 'leri

## Az. ResourceMover cmdlet 'Leri
### [Add-Azkaynakmovermoveresource](Add-AzResourceMoverMoveResource.md)
Taşıma koleksiyonundaki bir taşıma kaynağı oluşturur veya güncelleştirir.

### [Get-Azkaynakmovermovecollection](Get-AzResourceMoverMoveCollection.md)
Taşıma koleksiyonunu alır.

### [Get-Azkaynakmovermoveresource](Get-AzResourceMoverMoveResource.md)
Kaynağı taşı.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Çözülmemiş bağımlılıkların listesini alır.

### [Invoke-Azkaynakmovercommit](Invoke-AzResourceMoverCommit.md)
İstek gövdesine dahil edilen kaynak kümesini kaydeder.
Kayıt işlemi, moveState 'in ' CommitPending ' veya ' CommitFailed ' 'taki moveResource 'ta tetiklenir, moveResource moveState 'in başarılı bir şekilde tamamlanması için geçiş yapma.
Kullanıcıya yardımcı olmak için, yalnızca validateOnly özelliği true olarak ayarlanmış olan işlem çağrı yapabilir.

### [Invoke-Azkaynakmoverdiscard](Invoke-AzResourceMoverDiscard.md)
İstek gövdesine dahil edilen kaynak kümesini atar.
At işlemi, moveState ' CommitPending ' veya ' DiscardFailed ' içindeki moveResource 'da tetiklenir, moveResource moveState 'in başarılı bir şekilde tamamlanmasında MovePending 'a geçiş yapılır.
Kullanıcıya yardımcı olmak için, yalnızca validateOnly özelliği true olarak ayarlanmış olan işlem çağrı yapabilir.

### [Invoke-Azresourcesmoverınitiatetaþý](Invoke-AzResourceMoverInitiateMove.md)
İstek gövdesine dahil edilen kaynak kümesini taşıma.
Taşıma işlemi, moveResource 'ın Slaytbekliyor ' veya ' MoveFailed 'tekilerilerilerilerilerileriyle tetiklenir, bu da moveResource.
Kullanıcıya yardımcı olmak için, yalnızca validateOnly özelliği true olarak ayarlanmış olan işlem çağrı yapabilir.

### [Invoke-Azkaynakmoverprepare](Invoke-AzResourceMoverPrepare.md)
İstek gövdesine dahil edilen kaynak kümesine hazırlanmaya başlatır.
Prepare işlemi, moveState 'in ' PreparePending ' veya ' PrepareFailed ' işleminde bulunan moveResource 'dır, moveResource.
Kullanıcıya yardımcı olmak için, yalnızca validateOnly özelliği true olarak ayarlanmış olan işlem çağrı yapabilir.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Bir taşıma koleksiyonu oluşturur veya güncelleştirir.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Taşıma koleksiyonunu siler.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Taşıma koleksiyonundan taşıma kaynağı siler.

### [Resolve-Azkaynakmovermovecollectiondependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Taşıma koleksiyonundaki Taşıveresoallerin bağımlılıklarını hesaplar, çözümler ve doğrular.

