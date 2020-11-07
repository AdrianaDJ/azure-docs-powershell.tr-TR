---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 3220ef801ff86a3fb95a4595efd8c94330bfcba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762148"
---
# <span data-ttu-id="1ffb5-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ffb5-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="1ffb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ffb5-102">SYNOPSIS</span></span>
<span data-ttu-id="1ffb5-103">Bir kasaya yönelik yedek koruma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ffb5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ffb5-104">SYNTAX</span></span>

### <span data-ttu-id="1ffb5-105">NoParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1ffb5-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ffb5-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="1ffb5-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ffb5-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="1ffb5-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ffb5-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="1ffb5-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ffb5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ffb5-109">DESCRIPTION</span></span>
<span data-ttu-id="1ffb5-110">**Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet 'i, kasa Için Azure yedekleme koruma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>

<span data-ttu-id="1ffb5-111">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1ffb5-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ffb5-112">EXAMPLES</span></span>

### <span data-ttu-id="1ffb5-113">Örnek 1: kasadaki tüm ilkeleri alma</span><span class="sxs-lookup"><span data-stu-id="1ffb5-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="1ffb5-114">Bu komut kasada oluşturulan tüm koruma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="1ffb5-115">Örnek 2: belirli bir ilke edinin</span><span class="sxs-lookup"><span data-stu-id="1ffb5-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="1ffb5-116">Bu komut DefaultPolicy adlı koruma ilkesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="1ffb5-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ffb5-117">PARAMETERS</span></span>

### <span data-ttu-id="1ffb5-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="1ffb5-118">-BackupManagementType</span></span>
<span data-ttu-id="1ffb5-119">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="1ffb5-120">Şu anda yalnızca AzureVM destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-120">Currently, only AzureVM is supported.</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffb5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ffb5-121">-DefaultProfile</span></span>
<span data-ttu-id="1ffb5-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffb5-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ffb5-123">-Name</span></span>
<span data-ttu-id="1ffb5-124">İlkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-124">Specifies the name of the policy.</span></span>

```yaml
Type: String
Parameter Sets: PolicyNameParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffb5-125">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="1ffb5-125">-WorkloadType</span></span>
<span data-ttu-id="1ffb5-126">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-126">Specifies the workload type.</span></span>
<span data-ttu-id="1ffb5-127">Şu anda yalnızca AzureVM destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-127">Currently, only AzureVM is supported.</span></span>

```yaml
Type: WorkloadType
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffb5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ffb5-128">CommonParameters</span></span>
<span data-ttu-id="1ffb5-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ffb5-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ffb5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ffb5-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ffb5-131">INPUTS</span></span>

### <span data-ttu-id="1ffb5-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1ffb5-132">None</span></span>
<span data-ttu-id="1ffb5-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1ffb5-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ffb5-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ffb5-134">OUTPUTS</span></span>

### <span data-ttu-id="1ffb5-135">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="1ffb5-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="1ffb5-136">System. Koleksiyonlar. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. modeller. PolicyBase]</span><span class="sxs-lookup"><span data-stu-id="1ffb5-136">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase]</span></span>

## <span data-ttu-id="1ffb5-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ffb5-137">NOTES</span></span>

## <span data-ttu-id="1ffb5-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ffb5-138">RELATED LINKS</span></span>

[<span data-ttu-id="1ffb5-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ffb5-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1ffb5-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ffb5-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1ffb5-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ffb5-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


