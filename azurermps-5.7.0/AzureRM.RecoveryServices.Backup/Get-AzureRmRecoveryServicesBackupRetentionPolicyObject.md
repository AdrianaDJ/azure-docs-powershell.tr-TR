---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 83ed9062c5ad4beb0dff9c9c89b79a443cc68a52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587490"
---
# <span data-ttu-id="e9ce0-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="e9ce0-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="e9ce0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ce0-103">Temel bekletme ilkesi nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9ce0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9ce0-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9ce0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9ce0-105">DESCRIPTION</span></span>
<span data-ttu-id="e9ce0-106">**Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet 'i bir temel **AzureRMRecoveryServicesRetentionPolicyObject** alır.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="e9ce0-107">Bu nesne sistemde kalıcı değil.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="e9ce0-108">Bu, yeni bir yedekleme ilkesi oluşturmak için New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet 'i değiştirebileceğiniz ve kullanabileceğiniz geçici bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="e9ce0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9ce0-109">EXAMPLES</span></span>

### <span data-ttu-id="e9ce0-110">Örnek 1: yedekleme koruma ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e9ce0-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="e9ce0-111">İlk komut bekletme ilkesi nesnesini alır ve $RetPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="e9ce0-112">İkinci komut, bekletme ilkesi nesnesinin süresini 365 gün olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-112">The second command sets the duration for the retention policy object to 365 days.</span></span>

<span data-ttu-id="e9ce0-113">Üçüncü komut zamanlama İlkesi nesnesini alır ve $SchPol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="e9ce0-114">Son komut, önceki komutlarla oluşturulan bekletme ilkesini ve zamanlama ilkesini kullanarak yedek koruma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="e9ce0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9ce0-115">PARAMETERS</span></span>

### <span data-ttu-id="e9ce0-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e9ce0-116">-BackupManagementType</span></span>
<span data-ttu-id="e9ce0-117">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="e9ce0-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e9ce0-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e9ce0-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e9ce0-119">AzureVM</span></span> 
- <span data-ttu-id="e9ce0-120">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="e9ce0-120">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ce0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9ce0-121">-DefaultProfile</span></span>
<span data-ttu-id="e9ce0-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9ce0-123">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="e9ce0-123">-WorkloadType</span></span>
<span data-ttu-id="e9ce0-124">İş yükü türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-124">Specifies the workload type.</span></span>
<span data-ttu-id="e9ce0-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e9ce0-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e9ce0-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e9ce0-126">AzureVM</span></span> 
- <span data-ttu-id="e9ce0-127">Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="e9ce0-127">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ce0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ce0-128">CommonParameters</span></span>
<span data-ttu-id="e9ce0-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ce0-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9ce0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ce0-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9ce0-131">INPUTS</span></span>

### <span data-ttu-id="e9ce0-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e9ce0-132">None</span></span>
<span data-ttu-id="e9ce0-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9ce0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9ce0-134">OUTPUTS</span></span>

### <span data-ttu-id="e9ce0-135">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. modeller. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="e9ce0-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="e9ce0-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9ce0-136">NOTES</span></span>

## <span data-ttu-id="e9ce0-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9ce0-137">RELATED LINKS</span></span>

[<span data-ttu-id="e9ce0-138">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="e9ce0-138">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="e9ce0-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e9ce0-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)


