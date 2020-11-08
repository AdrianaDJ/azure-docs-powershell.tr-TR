---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: 1e10fe2aa534e236c99468ec672e6a0eeadae469
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104719"
---
# <span data-ttu-id="7dea5-101">Get-AzRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="7dea5-101">Get-AzRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="7dea5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dea5-102">SYNOPSIS</span></span>
<span data-ttu-id="7dea5-103">ARM kaynağınızın yedeklenip yedeklenmediğini denetler.</span><span class="sxs-lookup"><span data-stu-id="7dea5-103">Checks whether your ARM resource is backed up or not.</span></span>

## <span data-ttu-id="7dea5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7dea5-104">SYNTAX</span></span>

### <span data-ttu-id="7dea5-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7dea5-105">Name (Default)</span></span>
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dea5-106">Idworkload</span><span class="sxs-lookup"><span data-stu-id="7dea5-106">IdWorkload</span></span>
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dea5-107">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="7dea5-107">Id</span></span>
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7dea5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7dea5-108">DESCRIPTION</span></span>
<span data-ttu-id="7dea5-109">Belirtilen kaynak, abonelikteki herhangi bir kurtarma hizmetleri Kasası altında korunmuyorsa komut null/boş döndürür.</span><span class="sxs-lookup"><span data-stu-id="7dea5-109">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="7dea5-110">Korunmuşsa, ilgili kasa ayrıntıları geri döndürülecek.</span><span class="sxs-lookup"><span data-stu-id="7dea5-110">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="7dea5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7dea5-111">EXAMPLES</span></span>

### <span data-ttu-id="7dea5-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7dea5-112">Example 1</span></span>
```
PS C:\> $status = Get-AzRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="7dea5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7dea5-113">PARAMETERS</span></span>

### <span data-ttu-id="7dea5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dea5-114">-DefaultProfile</span></span>
<span data-ttu-id="7dea5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7dea5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dea5-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="7dea5-116">-Name</span></span>
<span data-ttu-id="7dea5-117">Aboneliğindeki bazı kurtarma hizmetleri Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken Azure kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="7dea5-117">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dea5-118">-Korunabilir NesneAdı</span><span class="sxs-lookup"><span data-stu-id="7dea5-118">-ProtectableObjectName</span></span>
<span data-ttu-id="7dea5-119">Aboneliğindeki bazı kurtarma hizmetleri Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken Azure kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="7dea5-119">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dea5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dea5-120">-ResourceGroupName</span></span>
<span data-ttu-id="7dea5-121">Aboneliğindeki bazı RecoveryServices Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7dea5-121">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dea5-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7dea5-122">-ResourceId</span></span>
<span data-ttu-id="7dea5-123">Abonelikteki bazı RecoveryServices Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken Azure kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7dea5-123">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload, Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dea5-124">-Tür</span><span class="sxs-lookup"><span data-stu-id="7dea5-124">-Type</span></span>
<span data-ttu-id="7dea5-125">Aboneliğindeki bazı kurtarma hizmetleri Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken Azure kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="7dea5-125">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, IdWorkload
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dea5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dea5-126">CommonParameters</span></span>
<span data-ttu-id="7dea5-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7dea5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dea5-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7dea5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dea5-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7dea5-129">INPUTS</span></span>

### <span data-ttu-id="7dea5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7dea5-130">System.String</span></span>

## <span data-ttu-id="7dea5-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7dea5-131">OUTPUTS</span></span>

### <span data-ttu-id="7dea5-132">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="7dea5-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="7dea5-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7dea5-133">NOTES</span></span>

## <span data-ttu-id="7dea5-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7dea5-134">RELATED LINKS</span></span>
