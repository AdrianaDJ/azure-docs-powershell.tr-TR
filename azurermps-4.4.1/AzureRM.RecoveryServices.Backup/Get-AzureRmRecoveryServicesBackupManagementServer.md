---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: c76bd152f64b337ca818c9e86b14fddbdaaf38cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594207"
---
# <span data-ttu-id="9e778-101">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="9e778-101">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="9e778-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e778-102">SYNOPSIS</span></span>
<span data-ttu-id="9e778-103">SCDPM ve Azure yedekleme yönetim sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="9e778-103">Gets SCDPM and Azure Backup management servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e778-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e778-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e778-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e778-105">DESCRIPTION</span></span>
<span data-ttu-id="9e778-106">**Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet 'Inde kaydedilen yedekleme yönetim sunucularının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="9e778-106">The **Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>

<span data-ttu-id="9e778-107">İki tür yedekleme yönetim sunucusu vardır: System Center Data Protection Manager (SCDPM) ve Azure yedekleme yönetim sunucuları.</span><span class="sxs-lookup"><span data-stu-id="9e778-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="9e778-108">Yedekleme yönetim sunucuları yedekleme düzenlemesini yönetmeye ayrı olarak yüklenir.</span><span class="sxs-lookup"><span data-stu-id="9e778-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>

<span data-ttu-id="9e778-109">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9e778-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9e778-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e778-110">EXAMPLES</span></span>

### <span data-ttu-id="9e778-111">Örnek 1: tüm yedekleme yönetim sunucularını alma</span><span class="sxs-lookup"><span data-stu-id="9e778-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

<span data-ttu-id="9e778-112">Bu komut, kasaya kaydedilmiş tüm yedek yönetim sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="9e778-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="9e778-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e778-113">PARAMETERS</span></span>

### <span data-ttu-id="9e778-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e778-114">-Name</span></span>
<span data-ttu-id="9e778-115">Alınacak yedekleme yönetimi sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e778-115">Specifies the name of the Backup management server to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e778-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e778-116">-DefaultProfile</span></span>
<span data-ttu-id="9e778-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e778-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e778-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e778-118">CommonParameters</span></span>
<span data-ttu-id="9e778-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e778-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e778-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e778-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e778-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e778-121">INPUTS</span></span>

## <span data-ttu-id="9e778-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e778-122">OUTPUTS</span></span>

### <span data-ttu-id="9e778-123">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="9e778-123">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

### <span data-ttu-id="9e778-124">System. Koleksiyonlar. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. BackupEngineBase]</span><span class="sxs-lookup"><span data-stu-id="9e778-124">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase]</span></span>

## <span data-ttu-id="9e778-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e778-125">NOTES</span></span>

## <span data-ttu-id="9e778-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e778-126">RELATED LINKS</span></span>

[<span data-ttu-id="9e778-127">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="9e778-127">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)


