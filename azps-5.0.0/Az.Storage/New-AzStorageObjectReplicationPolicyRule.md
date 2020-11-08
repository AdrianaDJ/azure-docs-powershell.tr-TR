---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277158"
---
# <span data-ttu-id="6301b-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6301b-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="6301b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6301b-102">SYNOPSIS</span></span>
<span data-ttu-id="6301b-103">Nesne çoğaltma ilkesi kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6301b-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="6301b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6301b-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6301b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6301b-105">DESCRIPTION</span></span>
<span data-ttu-id="6301b-106">**Get-AzStorageObjectReplicationPolicy** cmdlet 'i, Set-AzStorageObjectReplicationPolicy cmdlet 'te kullanılacak bir nesne çoğaltma ilkesi kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6301b-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="6301b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6301b-107">EXAMPLES</span></span>

### <span data-ttu-id="6301b-108">Örnek 1: yalnızca kaynak ve hedef hesapla bir nesne çoğaltma ilkesi kuralı oluşturma ve özelliklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="6301b-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="6301b-109">Bu komut, yalnızca kaynak ve hedef hesabı olan bir nesne çoğaltma ilkesi kuralı oluşturur ve özelliklerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6301b-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="6301b-110">Örnek 2: tüm özelliklerle nesne çoğaltma ilkesi kuralı oluşturma ve özelliklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="6301b-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="6301b-111">Bu komut tüm özelliklere sahip bir nesne çoğaltma ilkesi kuralı ve özelliklerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6301b-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="6301b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6301b-112">PARAMETERS</span></span>

### <span data-ttu-id="6301b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6301b-113">-DefaultProfile</span></span>
<span data-ttu-id="6301b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6301b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6301b-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="6301b-115">-DestinationContainer</span></span>
<span data-ttu-id="6301b-116">Çoğaltılacak hedef kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="6301b-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="6301b-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="6301b-117">-MinCreationTime</span></span>
<span data-ttu-id="6301b-118">Saatten sonra oluşturulan blob hedefte çoğaltılır.</span><span class="sxs-lookup"><span data-stu-id="6301b-118">Blobs created after the time will be replicated to the destination..</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6301b-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="6301b-119">-PrefixMatch</span></span>
<span data-ttu-id="6301b-120">Yalnızca adları belirtilen önekle başlayan blob 'ları çoğaltmak için sonuçları süzer.</span><span class="sxs-lookup"><span data-stu-id="6301b-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6301b-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="6301b-121">-RuleId</span></span>
<span data-ttu-id="6301b-122">Nesne çoğaltma kuralı kimliği.</span><span class="sxs-lookup"><span data-stu-id="6301b-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="6301b-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="6301b-123">-SourceContainer</span></span>
<span data-ttu-id="6301b-124">Çoğaltılacak kaynak kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="6301b-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="6301b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6301b-125">CommonParameters</span></span>
<span data-ttu-id="6301b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6301b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6301b-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6301b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6301b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6301b-128">INPUTS</span></span>

### <span data-ttu-id="6301b-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6301b-129">None</span></span>

## <span data-ttu-id="6301b-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6301b-130">OUTPUTS</span></span>

### <span data-ttu-id="6301b-131">Microsoft. Azure. Commands. Management. Storage. model. PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6301b-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="6301b-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6301b-132">NOTES</span></span>

## <span data-ttu-id="6301b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6301b-133">RELATED LINKS</span></span>
