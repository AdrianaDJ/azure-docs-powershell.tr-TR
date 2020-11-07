---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 5fd705d38f2deb232c9b62861804eb2830f45999
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764529"
---
# <span data-ttu-id="d97be-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d97be-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="d97be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d97be-102">SYNOPSIS</span></span>
<span data-ttu-id="d97be-103">Temel bekletme ilkesi nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="d97be-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d97be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d97be-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d97be-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d97be-105">DESCRIPTION</span></span>
<span data-ttu-id="d97be-106">**Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet 'i bir temel **AzureRMRecoveryServicesRetentionPolicyObject** alır.</span><span class="sxs-lookup"><span data-stu-id="d97be-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="d97be-107">Bu nesne sistemde kalıcı değil.</span><span class="sxs-lookup"><span data-stu-id="d97be-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="d97be-108">Bu, yeni bir yedekleme ilkesi oluşturmak için New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet 'i değiştirebileceğiniz ve kullanabileceğiniz geçici bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="d97be-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="d97be-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d97be-109">EXAMPLES</span></span>

### <span data-ttu-id="d97be-110">Örnek 1: yedekleme koruma ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d97be-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="d97be-111">İlk komut bekletme ilkesi nesnesini alır ve $RetPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d97be-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="d97be-112">İkinci komut, bekletme ilkesi nesnesinin süresini 365 gün olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d97be-112">The second command sets the duration for the retention policy object to 365 days.</span></span>

<span data-ttu-id="d97be-113">Üçüncü komut zamanlama İlkesi nesnesini alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d97be-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="d97be-114">Son komut, önceki komutlarla oluşturulan bekletme ilkesini ve zamanlama ilkesini kullanarak yedek koruma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d97be-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="d97be-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d97be-115">PARAMETERS</span></span>

### <span data-ttu-id="d97be-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d97be-116">-BackupManagementType</span></span>
<span data-ttu-id="d97be-117">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d97be-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="d97be-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d97be-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d97be-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d97be-119">AzureVM</span></span> 
- <span data-ttu-id="d97be-120">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="d97be-120">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97be-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d97be-121">-WorkloadType</span></span>
<span data-ttu-id="d97be-122">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d97be-122">Specifies the workload type.</span></span>
<span data-ttu-id="d97be-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d97be-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d97be-124">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d97be-124">AzureVM</span></span> 
- <span data-ttu-id="d97be-125">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="d97be-125">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97be-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97be-126">-DefaultProfile</span></span>
<span data-ttu-id="d97be-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d97be-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d97be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97be-128">CommonParameters</span></span>
<span data-ttu-id="d97be-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d97be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97be-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d97be-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97be-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d97be-131">INPUTS</span></span>

## <span data-ttu-id="d97be-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d97be-132">OUTPUTS</span></span>

### <span data-ttu-id="d97be-133">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. modeller. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="d97be-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="d97be-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d97be-134">NOTES</span></span>

## <span data-ttu-id="d97be-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d97be-135">RELATED LINKS</span></span>

[<span data-ttu-id="d97be-136">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="d97be-136">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="d97be-137">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d97be-137">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)


