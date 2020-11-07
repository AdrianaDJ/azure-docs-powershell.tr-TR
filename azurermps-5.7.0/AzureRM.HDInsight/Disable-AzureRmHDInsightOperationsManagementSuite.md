---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/disable-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c29c27ab7b2212670abf7e100678cdfdd5beb6cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591681"
---
# <span data-ttu-id="3a193-101">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="3a193-101">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="3a193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a193-102">SYNOPSIS</span></span>
<span data-ttu-id="3a193-103">Bir HDInsight kümesindeki Operations Management paketini (OMS) devre dışı bırakır ve ilgili Günlükler, etkinleştir sırasında belirtilen OMS çalışma alanına akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="3a193-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a193-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a193-104">SYNTAX</span></span>

```
Disable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a193-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a193-105">DESCRIPTION</span></span>
<span data-ttu-id="3a193-106">**Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet 'ı bir Azure HDInsight kümesindeki Operations Management Suite 'ı (OMS) devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="3a193-106">The **Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="3a193-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a193-107">EXAMPLES</span></span>

### <span data-ttu-id="3a193-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3a193-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="3a193-109">Operations Management Suite (OMS) HDInsight kümesinde devre dışı bırakılır ve ilgili Günlükler OMS çalışma alanına akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="3a193-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="3a193-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3a193-110">Example 2</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="3a193-111">Operations Management Suite (OMS) HDInsight kümesinde devre dışı bırakılır ve ilgili Günlükler OMS çalışma alanına akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="3a193-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="3a193-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a193-112">PARAMETERS</span></span>

### <span data-ttu-id="3a193-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a193-113">-DefaultProfile</span></span>
<span data-ttu-id="3a193-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3a193-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a193-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a193-115">-Name</span></span>
<span data-ttu-id="3a193-116">Operations Management Suite 'i devre dışı bırakacak kümenin adı (OMS).</span><span class="sxs-lookup"><span data-stu-id="3a193-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a193-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a193-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a193-118">Kümenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="3a193-118">The resource group of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a193-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a193-119">-Confirm</span></span>
<span data-ttu-id="3a193-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a193-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a193-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a193-121">-WhatIf</span></span>
<span data-ttu-id="3a193-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a193-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a193-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a193-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a193-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a193-124">CommonParameters</span></span>
<span data-ttu-id="3a193-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a193-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a193-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a193-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a193-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a193-127">INPUTS</span></span>

### <span data-ttu-id="3a193-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3a193-128">System.String</span></span>

## <span data-ttu-id="3a193-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a193-129">OUTPUTS</span></span>

### <span data-ttu-id="3a193-130">Microsoft. Azure. Management. HDInsight. model. OperationResource</span><span class="sxs-lookup"><span data-stu-id="3a193-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="3a193-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a193-131">NOTES</span></span>

## <span data-ttu-id="3a193-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a193-132">RELATED LINKS</span></span>
