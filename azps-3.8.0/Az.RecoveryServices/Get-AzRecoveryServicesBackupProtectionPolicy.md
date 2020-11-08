---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1b29bcc12c92b08e1c21dff4bb8b239fcc8f2bf6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104732"
---
# <span data-ttu-id="076db-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="076db-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="076db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="076db-102">SYNOPSIS</span></span>
<span data-ttu-id="076db-103">Bir kasaya yönelik yedek koruma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="076db-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="076db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="076db-104">SYNTAX</span></span>

### <span data-ttu-id="076db-105">NoParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="076db-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="076db-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="076db-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="076db-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="076db-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="076db-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="076db-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="076db-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="076db-109">DESCRIPTION</span></span>
<span data-ttu-id="076db-110">**Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet 'i kasa Için Azure yedekleme koruma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="076db-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="076db-111">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="076db-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="076db-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="076db-112">EXAMPLES</span></span>

### <span data-ttu-id="076db-113">Örnek 1: kasadaki tüm ilkeleri alma</span><span class="sxs-lookup"><span data-stu-id="076db-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="076db-114">Bu komut kasada oluşturulan tüm koruma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="076db-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="076db-115">Örnek 2: belirli bir ilke edinin</span><span class="sxs-lookup"><span data-stu-id="076db-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="076db-116">Bu komut DefaultPolicy adlı koruma ilkesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="076db-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="076db-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="076db-117">PARAMETERS</span></span>

### <span data-ttu-id="076db-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="076db-118">-BackupManagementType</span></span>
<span data-ttu-id="076db-119">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="076db-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="076db-120">Şu anda, yalnızca AzureVM, AzureStorage destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="076db-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="076db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="076db-121">-DefaultProfile</span></span>
<span data-ttu-id="076db-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="076db-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="076db-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="076db-123">-Name</span></span>
<span data-ttu-id="076db-124">İlkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="076db-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="076db-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="076db-125">-VaultId</span></span>
<span data-ttu-id="076db-126">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="076db-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="076db-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="076db-127">-WorkloadType</span></span>
<span data-ttu-id="076db-128">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="076db-128">Specifies the workload type.</span></span>
<span data-ttu-id="076db-129">Şu anda yalnızca AzureVM, AzureFiles destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="076db-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="076db-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="076db-130">CommonParameters</span></span>
<span data-ttu-id="076db-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="076db-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="076db-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="076db-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="076db-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="076db-133">INPUTS</span></span>

### <span data-ttu-id="076db-134">System. String</span><span class="sxs-lookup"><span data-stu-id="076db-134">System.String</span></span>

## <span data-ttu-id="076db-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="076db-135">OUTPUTS</span></span>

### <span data-ttu-id="076db-136">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="076db-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="076db-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="076db-137">NOTES</span></span>

## <span data-ttu-id="076db-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="076db-138">RELATED LINKS</span></span>

[<span data-ttu-id="076db-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="076db-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="076db-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="076db-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="076db-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="076db-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


