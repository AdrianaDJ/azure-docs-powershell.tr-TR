---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 1f67da2d15aca003853bcb21846535bad4e2a066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759676"
---
# <span data-ttu-id="8f8ed-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="8f8ed-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="8f8ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="8f8ed-103">Azure sanal makine disklerinin çoğaltılacağı bir disk eşleme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="8f8ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f8ed-104">SYNTAX</span></span>

### <span data-ttu-id="8f8ed-105">AzureToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8f8ed-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f8ed-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8f8ed-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f8ed-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f8ed-107">DESCRIPTION</span></span>
<span data-ttu-id="8f8ed-108">Bir Azure sanal makine diskini, diski çoğaltmak için kullanılacak önbellek depolama hesabına ve hedef depolama hesabına (kurtarma bölgesi) eşleyen bir disk eşleme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="8f8ed-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f8ed-109">EXAMPLES</span></span>

### <span data-ttu-id="8f8ed-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8f8ed-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="8f8ed-111">Çoğaltılacak Azure sanal makine disklerinin disk eşleme nesnesi oluşturma. Azure-Azure EnableDr ile ve yeniden korumada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="8f8ed-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f8ed-112">PARAMETERS</span></span>

### <span data-ttu-id="8f8ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f8ed-113">-DefaultProfile</span></span>
<span data-ttu-id="8f8ed-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f8ed-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="8f8ed-115">-DiskId</span></span>
<span data-ttu-id="8f8ed-116">Yönetilen diskin disk kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-116">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8ed-117">-Logstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="8f8ed-117">-LogStorageAccountId</span></span>
<span data-ttu-id="8f8ed-118">Çoğaltma günlüklerinin depolanacağı günlük veya önbellek hesap kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8ed-119">-Manageddısk</span><span class="sxs-lookup"><span data-stu-id="8f8ed-119">-ManagedDisk</span></span>
<span data-ttu-id="8f8ed-120">Yönetilen disk için giriş olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-120">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8ed-121">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="8f8ed-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="8f8ed-122">Çoğaltılacak Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8ed-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="8f8ed-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="8f8ed-124">Çoğaltılmış yönetilen diskin hesap türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-124">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8ed-125">-Recoveryresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="8f8ed-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="8f8ed-126">Çoğaltılmış yönetilen disk için kurtarma kaynağı grup kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8ed-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="8f8ed-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="8f8ed-128">Çoğaltılmış yönetilen disk için kurtarma hedef diskini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-128">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8ed-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="8f8ed-129">-VhdUri</span></span>
<span data-ttu-id="8f8ed-130">Bu eşlemenin karşılık geldiği diskin VHD URI 'sini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8ed-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="8f8ed-131">-Confirm</span></span>
<span data-ttu-id="8f8ed-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8ed-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f8ed-133">-WhatIf</span></span>
<span data-ttu-id="8f8ed-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f8ed-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f8ed-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f8ed-136">CommonParameters</span></span>
<span data-ttu-id="8f8ed-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f8ed-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f8ed-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f8ed-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f8ed-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f8ed-139">INPUTS</span></span>

### <span data-ttu-id="8f8ed-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8f8ed-140">None</span></span>

## <span data-ttu-id="8f8ed-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f8ed-141">OUTPUTS</span></span>

### <span data-ttu-id="8f8ed-142">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="8f8ed-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="8f8ed-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f8ed-143">NOTES</span></span>

## <span data-ttu-id="8f8ed-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f8ed-144">RELATED LINKS</span></span>
