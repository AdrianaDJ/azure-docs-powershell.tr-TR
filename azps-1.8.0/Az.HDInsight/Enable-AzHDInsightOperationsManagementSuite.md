---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c7d357df084a3843f8accbd3f54cc8aba9085012
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916644"
---
# <span data-ttu-id="3cf7d-101">Enable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="3cf7d-101">Enable-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="3cf7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cf7d-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf7d-103">Bir HDInsight kümesinde Operations Management Suite (OMS) özelliğini etkinleştirir ve ilgili Günlükler etkinleştir sırasında belirtilen OMS çalışma alanına gönderilir.</span><span class="sxs-lookup"><span data-stu-id="3cf7d-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

## <span data-ttu-id="3cf7d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3cf7d-104">SYNTAX</span></span>

```
Enable-AzHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cf7d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3cf7d-105">DESCRIPTION</span></span>
<span data-ttu-id="3cf7d-106">**Enable-AzHDInsightOperationsManagementSuite** cmdlet 'i, bir Azure HDInsight kümesindeki Operations Management SUITE (OMS) özelliğini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="3cf7d-106">The **Enable-AzHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="3cf7d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3cf7d-107">EXAMPLES</span></span>

### <span data-ttu-id="3cf7d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3cf7d-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="3cf7d-109">Operations Management Suite (OMS), HDInsight kümesinde etkinleştirilecek ve ilgili Günlükler, 1d364e89-bb71-4503-aa3d-a23535aea7bd kimliğine sahip OMS çalışma alanına gönderilecektir.</span><span class="sxs-lookup"><span data-stu-id="3cf7d-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="3cf7d-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3cf7d-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="3cf7d-111">Operations Management Suite (OMS), HDInsight kümesinde etkinleştirilecek ve ilgili Günlükler, 1d364e89-bb71-4503-aa3d-a23535aea7bd kimliğine sahip OMS çalışma alanına gönderilecektir.</span><span class="sxs-lookup"><span data-stu-id="3cf7d-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="3cf7d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3cf7d-112">PARAMETERS</span></span>

### <span data-ttu-id="3cf7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf7d-113">-DefaultProfile</span></span>
<span data-ttu-id="3cf7d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3cf7d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cf7d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="3cf7d-115">-Name</span></span>
<span data-ttu-id="3cf7d-116">Operations Management Suite 'i (OMS) etkinleştirecek kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="3cf7d-116">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="3cf7d-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="3cf7d-117">-PrimaryKey</span></span>
<span data-ttu-id="3cf7d-118">Operations Management Suite (OMS) çalışma alanının birincil anahtarı.</span><span class="sxs-lookup"><span data-stu-id="3cf7d-118">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="3cf7d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf7d-119">-ResourceGroupName</span></span>
<span data-ttu-id="3cf7d-120">Kümenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="3cf7d-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="3cf7d-121">-</span><span class="sxs-lookup"><span data-stu-id="3cf7d-121">-WorkspaceId</span></span>
<span data-ttu-id="3cf7d-122">Operations Management Suite (OMS) çalışma alanı kimliği.</span><span class="sxs-lookup"><span data-stu-id="3cf7d-122">The id of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="3cf7d-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="3cf7d-123">-Confirm</span></span>
<span data-ttu-id="3cf7d-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3cf7d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf7d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf7d-125">-WhatIf</span></span>
<span data-ttu-id="3cf7d-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3cf7d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cf7d-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3cf7d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf7d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf7d-128">CommonParameters</span></span>
<span data-ttu-id="3cf7d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3cf7d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf7d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf7d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf7d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3cf7d-131">INPUTS</span></span>

### <span data-ttu-id="3cf7d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf7d-132">System.String</span></span>

## <span data-ttu-id="3cf7d-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3cf7d-133">OUTPUTS</span></span>

### <span data-ttu-id="3cf7d-134">Microsoft. Azure. Management. HDInsight. model. OperationResource</span><span class="sxs-lookup"><span data-stu-id="3cf7d-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="3cf7d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3cf7d-135">NOTES</span></span>

## <span data-ttu-id="3cf7d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3cf7d-136">RELATED LINKS</span></span>