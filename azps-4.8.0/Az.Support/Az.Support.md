---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266719"
---
# Az. destek modülü
## Tanım
Bu bölümdeki konular, Azure destek biletlerini Azure Resource Manager (ARM) çerçevesinde oluşturmak ve yönetmek için Azure PowerShell cmdlet 'lerini belgeleyin. Microsoft. Azure. Commands. support ad alanında cmdlet 'ler var

## Az. destek cmdlet 'Leri
### [Get-AzSupportService](Get-AzSupportService.md)
Desteği sağlanan Azure hizmetlerinin geçerli listesini alır. Her Azure hizmetinin, sorun sınıflandırması denen kendi kategorileri vardır. Get-AzSupportProblemClassification kullanarak bir hizmetin geçerli sorun sınıflandırması listesini alın. Yeni-AzSupportTicket kullanarak yeni bir destek bileti oluşturmak için hizmet ve sorun sınıflandırması GUID 'sini kullanabilirsiniz.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Bir Azure hizmeti için geçerli sorun sınıflandırması listesini alır. Yeni-AzSupportTicket kullanarak yeni bir destek bileti oluşturmak için hizmet ve sorun sınıflandırması GUID 'sini kullanabilirsiniz. 

### [Yeni-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Destek kişi profili nesnesi oluşturmak için yardımcı cmdlet. Bu nesneyi New-AzSupportTicket cmdlet için kullanabilirsiniz.

### [Yeni-Azsupportbilet](New-AzSupportTicket.md)
Yeni bir Azure destek bileti oluşturur. Bu işlem, Azure [Yeni destek isteği sayfasının](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)davranışındaki modellenir.

### [Get-Azsupportbilet](Get-AzSupportTicket.md)
Destek biletleri listesini alır. Bilet adına göre tam destek bileti alabilir veya destek biletlerini *duruma* veya *CreatedDate* 'e göre filtreleyebilirsiniz.

### [Update-Azsupportbilet](Update-AzSupportTicket.md)
Destek biletinin önem derecesini, durumunu veya müşteri iletişim ayrıntılarını güncelleyin.

### [Get-Azsupportbilet Iletişimi](Get-AzSupportTicketCommunication.md)
Destek bileti için iletişimleri alır. *CreatedDate*   veya *communicationtype* ile destek bileti iletişimini de filtreleyebilirsiniz. 

### [Yeni-Azsupportbilet Iletişimi](New-AzSupportTicketCommunication.md)
Azure destek biletini yeni bir müşteri iletişimi ekler. 



