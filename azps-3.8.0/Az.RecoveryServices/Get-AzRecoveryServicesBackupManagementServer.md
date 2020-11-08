---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096363"
---
# <span data-ttu-id="e5d81-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="e5d81-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="e5d81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5d81-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d81-103">SCDPM ve Azure yedekleme yönetim sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="e5d81-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="e5d81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5d81-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5d81-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5d81-105">DESCRIPTION</span></span>
<span data-ttu-id="e5d81-106">**Get-AzRecoveryServicesBackupManagementServer** cmdlet 'Inde kaydedilen yedekleme yönetim sunucularının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="e5d81-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="e5d81-107">İki tür yedekleme yönetim sunucusu vardır: System Center Data Protection Manager (SCDPM) ve Azure yedekleme yönetim sunucuları.</span><span class="sxs-lookup"><span data-stu-id="e5d81-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="e5d81-108">Yedekleme yönetim sunucuları yedekleme düzenlemesini yönetmeye ayrı olarak yüklenir.</span><span class="sxs-lookup"><span data-stu-id="e5d81-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="e5d81-109">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e5d81-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e5d81-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5d81-110">EXAMPLES</span></span>

### <span data-ttu-id="e5d81-111">Örnek 1: tüm yedekleme yönetim sunucularını alma</span><span class="sxs-lookup"><span data-stu-id="e5d81-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="e5d81-112">Bu komut, kasaya kaydedilmiş tüm yedek yönetim sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="e5d81-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="e5d81-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5d81-113">PARAMETERS</span></span>

### <span data-ttu-id="e5d81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d81-114">-DefaultProfile</span></span>
<span data-ttu-id="e5d81-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5d81-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d81-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5d81-116">-Name</span></span>
<span data-ttu-id="e5d81-117">Alınacak yedekleme yönetimi sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5d81-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="e5d81-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e5d81-118">-VaultId</span></span>
<span data-ttu-id="e5d81-119">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e5d81-119">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d81-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d81-120">CommonParameters</span></span>
<span data-ttu-id="e5d81-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5d81-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d81-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e5d81-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d81-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5d81-123">INPUTS</span></span>

### <span data-ttu-id="e5d81-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e5d81-124">System.String</span></span>

## <span data-ttu-id="e5d81-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5d81-125">OUTPUTS</span></span>

### <span data-ttu-id="e5d81-126">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="e5d81-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="e5d81-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5d81-127">NOTES</span></span>

## <span data-ttu-id="e5d81-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5d81-128">RELATED LINKS</span></span>

[<span data-ttu-id="e5d81-129">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="e5d81-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


