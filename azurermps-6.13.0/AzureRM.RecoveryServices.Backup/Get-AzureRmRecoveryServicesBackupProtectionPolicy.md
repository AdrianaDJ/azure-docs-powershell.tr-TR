---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d08bd0a02878b1b99b3243e80512df30eca6e1c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590084"
---
# <span data-ttu-id="15d31-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="15d31-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="15d31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15d31-102">SYNOPSIS</span></span>
<span data-ttu-id="15d31-103">Bir kasaya yönelik yedek koruma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="15d31-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15d31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15d31-104">SYNTAX</span></span>

### <span data-ttu-id="15d31-105">NoParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="15d31-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15d31-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="15d31-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15d31-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="15d31-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15d31-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="15d31-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15d31-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="15d31-109">DESCRIPTION</span></span>
<span data-ttu-id="15d31-110">**Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet 'i, kasa Için Azure yedekleme koruma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="15d31-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="15d31-111">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="15d31-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="15d31-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15d31-112">EXAMPLES</span></span>

### <span data-ttu-id="15d31-113">Örnek 1: kasadaki tüm ilkeleri alma</span><span class="sxs-lookup"><span data-stu-id="15d31-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="15d31-114">Bu komut kasada oluşturulan tüm koruma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="15d31-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="15d31-115">Örnek 2: belirli bir ilke edinin</span><span class="sxs-lookup"><span data-stu-id="15d31-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="15d31-116">Bu komut DefaultPolicy adlı koruma ilkesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="15d31-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="15d31-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15d31-117">PARAMETERS</span></span>

### <span data-ttu-id="15d31-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="15d31-118">-BackupManagementType</span></span>
<span data-ttu-id="15d31-119">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="15d31-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="15d31-120">Şu anda, yalnızca AzureVM, AzureStorage destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="15d31-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d31-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d31-121">-DefaultProfile</span></span>
<span data-ttu-id="15d31-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15d31-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15d31-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="15d31-123">-Name</span></span>
<span data-ttu-id="15d31-124">İlkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15d31-124">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d31-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="15d31-125">-VaultId</span></span>
<span data-ttu-id="15d31-126">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="15d31-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="15d31-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="15d31-127">-WorkloadType</span></span>
<span data-ttu-id="15d31-128">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="15d31-128">Specifies the workload type.</span></span>
<span data-ttu-id="15d31-129">Şu anda yalnızca AzureVM, AzureFiles destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="15d31-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d31-130">CommonParameters</span></span>
<span data-ttu-id="15d31-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15d31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d31-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15d31-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d31-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15d31-133">INPUTS</span></span>

### <span data-ttu-id="15d31-134">System. String</span><span class="sxs-lookup"><span data-stu-id="15d31-134">System.String</span></span>
<span data-ttu-id="15d31-135">Parametreler: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="15d31-135">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="15d31-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15d31-136">OUTPUTS</span></span>

### <span data-ttu-id="15d31-137">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="15d31-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="15d31-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15d31-138">NOTES</span></span>

## <span data-ttu-id="15d31-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15d31-139">RELATED LINKS</span></span>

[<span data-ttu-id="15d31-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="15d31-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="15d31-141">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="15d31-141">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="15d31-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="15d31-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


