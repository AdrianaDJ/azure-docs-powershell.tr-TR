---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 341b222c8b5e85a4b5f5221c34d6f45cd2993c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933009"
---
# <span data-ttu-id="a4565-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="a4565-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="a4565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4565-102">SYNOPSIS</span></span>
<span data-ttu-id="a4565-103">SCDPM ve Azure yedekleme yönetim sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="a4565-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="a4565-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4565-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4565-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4565-105">DESCRIPTION</span></span>
<span data-ttu-id="a4565-106">**Get-AzRecoveryServicesBackupManagementServer** cmdlet 'Inde kaydedilen yedekleme yönetim sunucularının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="a4565-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="a4565-107">İki tür yedekleme yönetim sunucusu vardır: System Center Data Protection Manager (SCDPM) ve Azure yedekleme yönetim sunucuları.</span><span class="sxs-lookup"><span data-stu-id="a4565-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="a4565-108">Yedekleme yönetim sunucuları yedekleme düzenlemesini yönetmeye ayrı olarak yüklenir.</span><span class="sxs-lookup"><span data-stu-id="a4565-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="a4565-109">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a4565-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a4565-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4565-110">EXAMPLES</span></span>

### <span data-ttu-id="a4565-111">Örnek 1: tüm yedekleme yönetim sunucularını alma</span><span class="sxs-lookup"><span data-stu-id="a4565-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="a4565-112">Bu komut, kasaya kaydedilmiş tüm yedek yönetim sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="a4565-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="a4565-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4565-113">PARAMETERS</span></span>

### <span data-ttu-id="a4565-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4565-114">-DefaultProfile</span></span>
<span data-ttu-id="a4565-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a4565-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4565-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="a4565-116">-Name</span></span>
<span data-ttu-id="a4565-117">Alınacak yedekleme yönetimi sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4565-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="a4565-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a4565-118">-VaultId</span></span>
<span data-ttu-id="a4565-119">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a4565-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a4565-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4565-120">CommonParameters</span></span>
<span data-ttu-id="a4565-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4565-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4565-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4565-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4565-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4565-123">INPUTS</span></span>

### <span data-ttu-id="a4565-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a4565-124">System.String</span></span>

## <span data-ttu-id="a4565-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4565-125">OUTPUTS</span></span>

### <span data-ttu-id="a4565-126">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="a4565-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="a4565-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4565-127">NOTES</span></span>

## <span data-ttu-id="a4565-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4565-128">RELATED LINKS</span></span>

[<span data-ttu-id="a4565-129">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="a4565-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


