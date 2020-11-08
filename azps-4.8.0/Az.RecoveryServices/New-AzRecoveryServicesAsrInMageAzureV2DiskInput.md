---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265803"
---
# <span data-ttu-id="a18a1-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="a18a1-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="a18a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a18a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a18a1-103">VMWare sanal makine disklerinin çoğaltılması için bir disk eşleme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a18a1-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="a18a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a18a1-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a18a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a18a1-105">DESCRIPTION</span></span>
<span data-ttu-id="a18a1-106">Bir vMWare sanal makine diskini, diski çoğaltmak için kullanılacak önbellek depolama hesabına ve hedef yönetilen disk türüne (kurtarma bölgesi) eşleyen bir disk eşleme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a18a1-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="a18a1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a18a1-107">EXAMPLES</span></span>

### <span data-ttu-id="a18a1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a18a1-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="a18a1-109">Çoğaltılacak vMWare sanal makine disklerinin disk eşleme nesnesi oluşturma. VMWare makinesi için korumayı etkinleştirme sırasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a18a1-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="a18a1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a18a1-110">PARAMETERS</span></span>

### <span data-ttu-id="a18a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a18a1-111">-DefaultProfile</span></span>
<span data-ttu-id="a18a1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a18a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a18a1-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="a18a1-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="a18a1-114">Yönetilen disklerin şifrelenmesi için kullanılacak disk şifrelemesi kümesinin kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a18a1-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18a1-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="a18a1-115">-DiskId</span></span>
<span data-ttu-id="a18a1-116">Bu eşlemenin karşılık geldiği diskin DiskID 'yi belirtin.</span><span class="sxs-lookup"><span data-stu-id="a18a1-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="a18a1-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="a18a1-117">-DiskType</span></span>
<span data-ttu-id="a18a1-118">Kurtarma diski türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a18a1-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="a18a1-119">-Logstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="a18a1-119">-LogStorageAccountId</span></span>
<span data-ttu-id="a18a1-120">Çoğaltma günlüklerinin depolanacağı günlük veya önbellek hesap kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a18a1-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="a18a1-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="a18a1-121">-Confirm</span></span>
<span data-ttu-id="a18a1-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a18a1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a18a1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a18a1-123">-WhatIf</span></span>
<span data-ttu-id="a18a1-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a18a1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a18a1-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a18a1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a18a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18a1-126">CommonParameters</span></span>
<span data-ttu-id="a18a1-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a18a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18a1-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a18a1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18a1-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a18a1-129">INPUTS</span></span>

### <span data-ttu-id="a18a1-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a18a1-130">None</span></span>

## <span data-ttu-id="a18a1-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a18a1-131">OUTPUTS</span></span>

### <span data-ttu-id="a18a1-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="a18a1-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="a18a1-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a18a1-133">NOTES</span></span>

## <span data-ttu-id="a18a1-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a18a1-134">RELATED LINKS</span></span>
