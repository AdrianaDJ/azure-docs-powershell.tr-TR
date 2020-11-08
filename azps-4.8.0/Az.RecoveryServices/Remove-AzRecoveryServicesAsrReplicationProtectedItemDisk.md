---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267660"
---
# <span data-ttu-id="8f285-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="8f285-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="8f285-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f285-102">SYNOPSIS</span></span>
<span data-ttu-id="8f285-103">Diskleri çoğaltma korumalı öğeye çıkarır.</span><span class="sxs-lookup"><span data-stu-id="8f285-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="8f285-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f285-104">SYNTAX</span></span>

### <span data-ttu-id="8f285-105">AzureToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8f285-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f285-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8f285-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f285-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f285-107">DESCRIPTION</span></span>
<span data-ttu-id="8f285-108">**Remove-Azrecoveryservicesasrreplicationkorumatemreplicationkorumalıdır** , diski ASR çoğaltması korumalı öğesinden çıkarır.</span><span class="sxs-lookup"><span data-stu-id="8f285-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="8f285-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f285-109">EXAMPLES</span></span>

### <span data-ttu-id="8f285-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8f285-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="8f285-111">Belirtilen diski yönetilmeyen diskteki koruma VM 'sinden kaldırmak için işlemi başlatın.</span><span class="sxs-lookup"><span data-stu-id="8f285-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="8f285-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8f285-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="8f285-113">Belirtilen diski yönetilen diskteki koruma VM 'sinden kaldırmak için işlemi başlatın.</span><span class="sxs-lookup"><span data-stu-id="8f285-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="8f285-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="8f285-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="8f285-115">Belirtilen diski kaldırmak için işlemi başlatır ve korunan diski Kaldır işlemini izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8f285-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="8f285-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f285-116">PARAMETERS</span></span>

### <span data-ttu-id="8f285-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="8f285-117">-Confirm</span></span>
<span data-ttu-id="8f285-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8f285-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f285-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f285-119">-DefaultProfile</span></span>
<span data-ttu-id="8f285-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f285-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f285-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="8f285-121">-DiskId</span></span>
<span data-ttu-id="8f285-122">Yönetilen disk kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f285-122">Specifies the list of managed disk Ids.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f285-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f285-123">-InputObject</span></span>
<span data-ttu-id="8f285-124">Cmdlet 'e giriş nesnesi: hangi diske karşılık gelen ASR çoğaltması korumalı öğe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8f285-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f285-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="8f285-125">-VhdUri</span></span>
<span data-ttu-id="8f285-126">VHD URI 'sinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f285-126">Specifies the list of vhd Uri's.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f285-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="8f285-127">-WaitForCompletion</span></span>
<span data-ttu-id="8f285-128">Tamamlanması Için bekle</span><span class="sxs-lookup"><span data-stu-id="8f285-128">Wait For Completion</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f285-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f285-129">-WhatIf</span></span>
<span data-ttu-id="8f285-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f285-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f285-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f285-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f285-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f285-132">CommonParameters</span></span>
<span data-ttu-id="8f285-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f285-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f285-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8f285-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f285-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f285-135">INPUTS</span></span>

### <span data-ttu-id="8f285-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="8f285-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8f285-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f285-137">OUTPUTS</span></span>

### <span data-ttu-id="8f285-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8f285-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8f285-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f285-139">NOTES</span></span>

## <span data-ttu-id="8f285-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f285-140">RELATED LINKS</span></span>
