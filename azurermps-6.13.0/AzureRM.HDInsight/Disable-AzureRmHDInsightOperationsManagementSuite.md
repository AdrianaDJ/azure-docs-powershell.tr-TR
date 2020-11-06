---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/disable-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: f701d0c5e0ea2d8f4ce5ded850d131c6c066e9ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590279"
---
# <span data-ttu-id="e4862-101">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="e4862-101">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="e4862-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4862-102">SYNOPSIS</span></span>
<span data-ttu-id="e4862-103">Bir HDInsight kümesindeki Operations Management paketini (OMS) devre dışı bırakır ve ilgili Günlükler, etkinleştir sırasında belirtilen OMS çalışma alanına akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="e4862-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4862-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4862-104">SYNTAX</span></span>

```
Disable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4862-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4862-105">DESCRIPTION</span></span>
<span data-ttu-id="e4862-106">**Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet 'ı bir Azure HDInsight kümesindeki Operations Management Suite 'ı (OMS) devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e4862-106">The **Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e4862-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4862-107">EXAMPLES</span></span>

### <span data-ttu-id="e4862-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e4862-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="e4862-109">Operations Management Suite (OMS) HDInsight kümesinde devre dışı bırakılır ve ilgili Günlükler OMS çalışma alanına akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="e4862-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="e4862-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e4862-110">Example 2</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="e4862-111">Operations Management Suite (OMS) HDInsight kümesinde devre dışı bırakılır ve ilgili Günlükler OMS çalışma alanına akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="e4862-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="e4862-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4862-112">PARAMETERS</span></span>

### <span data-ttu-id="e4862-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4862-113">-DefaultProfile</span></span>
<span data-ttu-id="e4862-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e4862-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4862-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4862-115">-Name</span></span>
<span data-ttu-id="e4862-116">Operations Management Suite 'i devre dışı bırakacak kümenin adı (OMS).</span><span class="sxs-lookup"><span data-stu-id="e4862-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="e4862-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4862-117">-ResourceGroupName</span></span>
<span data-ttu-id="e4862-118">Kümenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e4862-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="e4862-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="e4862-119">-Confirm</span></span>
<span data-ttu-id="e4862-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4862-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4862-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4862-121">-WhatIf</span></span>
<span data-ttu-id="e4862-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4862-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4862-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e4862-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4862-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4862-124">CommonParameters</span></span>
<span data-ttu-id="e4862-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4862-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4862-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4862-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4862-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4862-127">INPUTS</span></span>

### <span data-ttu-id="e4862-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e4862-128">System.String</span></span>

## <span data-ttu-id="e4862-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4862-129">OUTPUTS</span></span>

### <span data-ttu-id="e4862-130">Microsoft. Azure. Management. HDInsight. model. OperationResource</span><span class="sxs-lookup"><span data-stu-id="e4862-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="e4862-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4862-131">NOTES</span></span>

## <span data-ttu-id="e4862-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4862-132">RELATED LINKS</span></span>
