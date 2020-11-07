---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 4f4508d38e4401198359fc816d1a94875f70940a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751853"
---
# <span data-ttu-id="51929-101">Disable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="51929-101">Disable-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="51929-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51929-102">SYNOPSIS</span></span>
<span data-ttu-id="51929-103">Bir HDInsight kümesindeki Operations Management paketini (OMS) devre dışı bırakır ve ilgili Günlükler, etkinleştir sırasında belirtilen OMS çalışma alanına akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="51929-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

## <span data-ttu-id="51929-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51929-104">SYNTAX</span></span>

```
Disable-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51929-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="51929-105">DESCRIPTION</span></span>
<span data-ttu-id="51929-106">**Disable-AzHDInsightOperationsManagementSuite** cmdlet 'ı bir Azure HDInsight kümesindeki Operations Management Suite 'ı (OMS) devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="51929-106">The **Disable-AzHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="51929-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51929-107">EXAMPLES</span></span>

### <span data-ttu-id="51929-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="51929-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="51929-109">Operations Management Suite (OMS) HDInsight kümesinde devre dışı bırakılır ve ilgili Günlükler OMS çalışma alanına akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="51929-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="51929-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="51929-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="51929-111">Operations Management Suite (OMS) HDInsight kümesinde devre dışı bırakılır ve ilgili Günlükler OMS çalışma alanına akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="51929-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="51929-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51929-112">PARAMETERS</span></span>

### <span data-ttu-id="51929-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51929-113">-DefaultProfile</span></span>
<span data-ttu-id="51929-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="51929-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51929-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="51929-115">-Name</span></span>
<span data-ttu-id="51929-116">Operations Management Suite 'i devre dışı bırakacak kümenin adı (OMS).</span><span class="sxs-lookup"><span data-stu-id="51929-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51929-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51929-117">-ResourceGroupName</span></span>
<span data-ttu-id="51929-118">Kümenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="51929-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="51929-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="51929-119">-Confirm</span></span>
<span data-ttu-id="51929-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="51929-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51929-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51929-121">-WhatIf</span></span>
<span data-ttu-id="51929-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="51929-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51929-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="51929-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51929-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51929-124">CommonParameters</span></span>
<span data-ttu-id="51929-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51929-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51929-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51929-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51929-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51929-127">INPUTS</span></span>

### <span data-ttu-id="51929-128">System. String</span><span class="sxs-lookup"><span data-stu-id="51929-128">System.String</span></span>

## <span data-ttu-id="51929-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51929-129">OUTPUTS</span></span>

### <span data-ttu-id="51929-130">Microsoft. Azure. Management. HDInsight. model. OperationResource</span><span class="sxs-lookup"><span data-stu-id="51929-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="51929-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51929-131">NOTES</span></span>

## <span data-ttu-id="51929-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51929-132">RELATED LINKS</span></span>
