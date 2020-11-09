---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: d426cd18aaf3382939e55668b1c19938319a3c51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325051"
---
# <span data-ttu-id="b2422-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b2422-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="b2422-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2422-102">SYNOPSIS</span></span>
<span data-ttu-id="b2422-103">Temel bekletme ilkesi nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="b2422-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="b2422-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2422-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2422-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2422-105">DESCRIPTION</span></span>
<span data-ttu-id="b2422-106">**Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet 'i bir temel **AzureRMRecoveryServicesRetentionPolicyObject** alır.</span><span class="sxs-lookup"><span data-stu-id="b2422-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="b2422-107">Bu nesne sistemde kalıcı değil.</span><span class="sxs-lookup"><span data-stu-id="b2422-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="b2422-108">Bu, yeni bir yedekleme ilkesi oluşturmak için New-AzRecoveryServicesBackupProtectionPolicy cmdlet 'i değiştirebileceğiniz ve kullanabileceğiniz geçici bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="b2422-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="b2422-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2422-109">EXAMPLES</span></span>

### <span data-ttu-id="b2422-110">Örnek 1: yedekleme koruma ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b2422-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="b2422-111">İlk komut bekletme ilkesi nesnesini alır ve $RetPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b2422-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="b2422-112">İkinci komut, bekletme ilkesi nesnesinin süresini 365 gün olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b2422-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="b2422-113">Üçüncü komut zamanlama İlkesi nesnesini alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b2422-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="b2422-114">Son komut, önceki komutlarla oluşturulan bekletme ilkesini ve zamanlama ilkesini kullanarak yedek koruma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b2422-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="b2422-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2422-115">PARAMETERS</span></span>

### <span data-ttu-id="b2422-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b2422-116">-BackupManagementType</span></span>
<span data-ttu-id="b2422-117">Korunan kaynakların sınıfı.</span><span class="sxs-lookup"><span data-stu-id="b2422-117">The class of resources being protected.</span></span> <span data-ttu-id="b2422-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b2422-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2422-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b2422-119">AzureVM</span></span> 
- <span data-ttu-id="b2422-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="b2422-120">AzureWorkload</span></span>
- <span data-ttu-id="b2422-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="b2422-121">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2422-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2422-122">-DefaultProfile</span></span>
<span data-ttu-id="b2422-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2422-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2422-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="b2422-124">-WorkloadType</span></span>
<span data-ttu-id="b2422-125">Kaynağın iş yükü türü.</span><span class="sxs-lookup"><span data-stu-id="b2422-125">Workload type of the resource.</span></span> <span data-ttu-id="b2422-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b2422-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2422-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b2422-127">AzureVM</span></span> 
- <span data-ttu-id="b2422-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="b2422-128">AzureFiles</span></span>
- <span data-ttu-id="b2422-129">KLASÖRÜNÜN</span><span class="sxs-lookup"><span data-stu-id="b2422-129">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2422-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2422-130">CommonParameters</span></span>
<span data-ttu-id="b2422-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2422-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2422-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b2422-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2422-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2422-133">INPUTS</span></span>

### <span data-ttu-id="b2422-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b2422-134">None</span></span>

## <span data-ttu-id="b2422-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2422-135">OUTPUTS</span></span>

### <span data-ttu-id="b2422-136">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. modeller. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="b2422-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="b2422-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2422-137">NOTES</span></span>

## <span data-ttu-id="b2422-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2422-138">RELATED LINKS</span></span>

[<span data-ttu-id="b2422-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="b2422-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="b2422-140">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2422-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


