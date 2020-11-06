---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: 81f25eeb8d0e6b704c4ee6ef71cd2aebcf3624ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592216"
---
# <span data-ttu-id="72664-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="72664-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="72664-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72664-102">SYNOPSIS</span></span>
<span data-ttu-id="72664-103">Geçerli abonelikle ilişkilendirilmiş tüm Azure HDInsight kümelerini veya belirli bir kaynak grubunu alır ve listeler.</span><span class="sxs-lookup"><span data-stu-id="72664-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72664-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72664-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72664-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72664-105">DESCRIPTION</span></span>
<span data-ttu-id="72664-106">**Get-AzureRmHDInsightCluster** cmdlet 'i geçerli aboneliğin Azure HDInsight hizmeti kümelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="72664-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="72664-107">Belirli bir kümenin ayrıntılarını almak için *clustername* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="72664-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="72664-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72664-108">EXAMPLES</span></span>

### <span data-ttu-id="72664-109">Örnek 1: tüm Azure HDInsight kümelerini listeler</span><span class="sxs-lookup"><span data-stu-id="72664-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="72664-110">Bu komut tüm Azure HDInsight kümelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="72664-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="72664-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72664-111">PARAMETERS</span></span>

### <span data-ttu-id="72664-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="72664-112">-ClusterName</span></span>
<span data-ttu-id="72664-113">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72664-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72664-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72664-114">-ResourceGroupName</span></span>
<span data-ttu-id="72664-115">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72664-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72664-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72664-116">-DefaultProfile</span></span>
<span data-ttu-id="72664-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72664-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72664-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72664-118">CommonParameters</span></span>
<span data-ttu-id="72664-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72664-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72664-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72664-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72664-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72664-121">INPUTS</span></span>

## <span data-ttu-id="72664-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72664-122">OUTPUTS</span></span>

### <span data-ttu-id="72664-123">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightCluster]</span><span class="sxs-lookup"><span data-stu-id="72664-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster]</span></span>

## <span data-ttu-id="72664-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72664-124">NOTES</span></span>

## <span data-ttu-id="72664-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72664-125">RELATED LINKS</span></span>

[<span data-ttu-id="72664-126">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="72664-126">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="72664-127">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="72664-127">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


