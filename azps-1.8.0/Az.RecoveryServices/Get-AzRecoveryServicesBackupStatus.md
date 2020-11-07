---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: cd3e3e2ad33cb01935a2594571145f0667c9a3e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759684"
---
# <span data-ttu-id="36140-101">Get-AzRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="36140-101">Get-AzRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="36140-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36140-102">SYNOPSIS</span></span>
<span data-ttu-id="36140-103">ARM kaynağınızın yedeklenip yedeklenmediğini denetler.</span><span class="sxs-lookup"><span data-stu-id="36140-103">Checks whether your ARM resource is backed up or not.</span></span>

## <span data-ttu-id="36140-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36140-104">SYNTAX</span></span>

### <span data-ttu-id="36140-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="36140-105">Name (Default)</span></span>
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36140-106">Idworkload</span><span class="sxs-lookup"><span data-stu-id="36140-106">IdWorkload</span></span>
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36140-107">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="36140-107">Id</span></span>
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36140-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="36140-108">DESCRIPTION</span></span>
<span data-ttu-id="36140-109">Belirtilen kaynak, abonelikteki herhangi bir kurtarma hizmetleri Kasası altında korunmuyorsa komut null/boş döndürür.</span><span class="sxs-lookup"><span data-stu-id="36140-109">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="36140-110">Korunmuşsa, ilgili kasa ayrıntıları geri döndürülecek.</span><span class="sxs-lookup"><span data-stu-id="36140-110">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="36140-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36140-111">EXAMPLES</span></span>

### <span data-ttu-id="36140-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="36140-112">Example 1</span></span>
```
PS C:\> $status = Get-AzRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="36140-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36140-113">PARAMETERS</span></span>

### <span data-ttu-id="36140-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36140-114">-DefaultProfile</span></span>
<span data-ttu-id="36140-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36140-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36140-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="36140-116">-Name</span></span>
<span data-ttu-id="36140-117">Aboneliğindeki bazı kurtarma hizmetleri Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken Azure kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="36140-117">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="36140-118">-Korunabilir NesneAdı</span><span class="sxs-lookup"><span data-stu-id="36140-118">-ProtectableObjectName</span></span>
<span data-ttu-id="36140-119">Aboneliğindeki bazı kurtarma hizmetleri Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken Azure kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="36140-119">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="36140-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36140-120">-ResourceGroupName</span></span>
<span data-ttu-id="36140-121">Aboneliğindeki bazı RecoveryServices Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="36140-121">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="36140-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="36140-122">-ResourceId</span></span>
<span data-ttu-id="36140-123">Abonelikteki bazı RecoveryServices Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken Azure kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="36140-123">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="36140-124">-Tür</span><span class="sxs-lookup"><span data-stu-id="36140-124">-Type</span></span>
<span data-ttu-id="36140-125">Aboneliğindeki bazı kurtarma hizmetleri Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken Azure kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="36140-125">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="36140-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36140-126">CommonParameters</span></span>
<span data-ttu-id="36140-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36140-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36140-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36140-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36140-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36140-129">INPUTS</span></span>

### <span data-ttu-id="36140-130">System. String</span><span class="sxs-lookup"><span data-stu-id="36140-130">System.String</span></span>

## <span data-ttu-id="36140-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36140-131">OUTPUTS</span></span>

### <span data-ttu-id="36140-132">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="36140-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="36140-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36140-133">NOTES</span></span>

## <span data-ttu-id="36140-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36140-134">RELATED LINKS</span></span>
