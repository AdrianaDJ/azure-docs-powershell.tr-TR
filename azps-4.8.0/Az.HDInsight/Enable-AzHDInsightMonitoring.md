---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268239"
---
# <span data-ttu-id="bcbb1-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="bcbb1-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="bcbb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcbb1-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbb1-103">HDInsight kümesinde izlemeyi etkinleştirir ve ilgili Günlükler etkinleştir sırasında belirtilen izleme çalışma alanına gönderilir.</span><span class="sxs-lookup"><span data-stu-id="bcbb1-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="bcbb1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bcbb1-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bcbb1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bcbb1-105">DESCRIPTION</span></span>
<span data-ttu-id="bcbb1-106">**Enable-AzHDInsightMonitoring** cmdlet 'ı bir Azure HDInsight kümesinde izlemeyi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="bcbb1-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="bcbb1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bcbb1-107">EXAMPLES</span></span>

### <span data-ttu-id="bcbb1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bcbb1-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="bcbb1-109">İzleme, HDInsight kümesinde etkinleştirilecek ve ilgili Günlükler, kimlik 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="bcbb1-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="bcbb1-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bcbb1-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="bcbb1-111">İzleme, HDInsight kümesinde etkinleştirilecek ve ilgili Günlükler, kimlik 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="bcbb1-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="bcbb1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bcbb1-112">PARAMETERS</span></span>

### <span data-ttu-id="bcbb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbb1-113">-DefaultProfile</span></span>
<span data-ttu-id="bcbb1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bcbb1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcbb1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="bcbb1-115">-Name</span></span>
<span data-ttu-id="bcbb1-116">İzlemeyi etkinleştirmek için kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="bcbb1-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="bcbb1-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="bcbb1-117">-PrimaryKey</span></span>
<span data-ttu-id="bcbb1-118">İzleme çalışma alanının birincil anahtarı.</span><span class="sxs-lookup"><span data-stu-id="bcbb1-118">The primary key of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcbb1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcbb1-119">-ResourceGroupName</span></span>
<span data-ttu-id="bcbb1-120">Kümenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="bcbb1-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="bcbb1-121">-</span><span class="sxs-lookup"><span data-stu-id="bcbb1-121">-WorkspaceId</span></span>
<span data-ttu-id="bcbb1-122">İzleme çalışma alanının kimliği.</span><span class="sxs-lookup"><span data-stu-id="bcbb1-122">The id of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcbb1-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="bcbb1-123">-Confirm</span></span>
<span data-ttu-id="bcbb1-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bcbb1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcbb1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcbb1-125">-WhatIf</span></span>
<span data-ttu-id="bcbb1-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bcbb1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bcbb1-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bcbb1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcbb1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbb1-128">CommonParameters</span></span>
<span data-ttu-id="bcbb1-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bcbb1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbb1-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bcbb1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbb1-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bcbb1-131">INPUTS</span></span>

### <span data-ttu-id="bcbb1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bcbb1-132">System.String</span></span>

## <span data-ttu-id="bcbb1-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bcbb1-133">OUTPUTS</span></span>

### <span data-ttu-id="bcbb1-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bcbb1-134">System.Boolean</span></span>

## <span data-ttu-id="bcbb1-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bcbb1-135">NOTES</span></span>

## <span data-ttu-id="bcbb1-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bcbb1-136">RELATED LINKS</span></span>
