---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 9a65a82808c78fe878ba4a61f8be01f37fc11771
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938515"
---
# <span data-ttu-id="2c373-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="2c373-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="2c373-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c373-102">SYNOPSIS</span></span>
<span data-ttu-id="2c373-103">HDInsight kümesinde izlemeyi devre dışı bırakır ve ilgili Günlükler, etkinleştir sırasında belirtilen izleme çalışma alanına akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="2c373-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="2c373-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c373-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c373-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c373-105">DESCRIPTION</span></span>
<span data-ttu-id="2c373-106">**Disable-AzHDInsightMonitoring** cmdlet 'ı bir Azure HDInsight kümesindeki izlemeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="2c373-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2c373-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c373-107">EXAMPLES</span></span>

### <span data-ttu-id="2c373-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2c373-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="2c373-109">İzleme, HDInsight kümesinde devre dışı bırakılır ve ilgili Günlükler izleme çalışma alanına akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="2c373-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="2c373-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2c373-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="2c373-111">İzleme, HDInsight kümesinde devre dışı bırakılır ve ilgili Günlükler izleme çalışma alanına akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="2c373-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="2c373-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c373-112">PARAMETERS</span></span>

### <span data-ttu-id="2c373-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c373-113">-DefaultProfile</span></span>
<span data-ttu-id="2c373-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2c373-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c373-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c373-115">-Name</span></span>
<span data-ttu-id="2c373-116">Izlemeyi devre dışı bırakan kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="2c373-116">The name of the cluster to disable Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c373-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c373-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c373-118">Kümenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="2c373-118">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c373-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="2c373-119">-Confirm</span></span>
<span data-ttu-id="2c373-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2c373-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c373-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c373-121">-WhatIf</span></span>
<span data-ttu-id="2c373-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c373-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c373-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2c373-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c373-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c373-124">CommonParameters</span></span>
<span data-ttu-id="2c373-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c373-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c373-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2c373-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c373-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c373-127">INPUTS</span></span>

### <span data-ttu-id="2c373-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2c373-128">System.String</span></span>

## <span data-ttu-id="2c373-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c373-129">OUTPUTS</span></span>

### <span data-ttu-id="2c373-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c373-130">System.Boolean</span></span>

## <span data-ttu-id="2c373-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c373-131">NOTES</span></span>

## <span data-ttu-id="2c373-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c373-132">RELATED LINKS</span></span>
