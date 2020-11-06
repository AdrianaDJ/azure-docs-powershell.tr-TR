---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: a09da5122403d971d8b5d1abde79c8a9a95c3ecd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594280"
---
# <span data-ttu-id="71251-101">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="71251-101">Remove-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="71251-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71251-102">SYNOPSIS</span></span>
<span data-ttu-id="71251-103">Belirtilen HDInsight kümesini geçerli abonelikten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="71251-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71251-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71251-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71251-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="71251-105">DESCRIPTION</span></span>
<span data-ttu-id="71251-106">**Remove-AzureRmHDInsightCluster** cmdlet 'i, belirtilen HDInsight hizmet kümesini abonelikten çıkarır.</span><span class="sxs-lookup"><span data-stu-id="71251-106">The **Remove-AzureRmHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="71251-107">Bu işlem, kümedeki Hadoop Dağıtılmış dosya sisteminde (".) depolanan verileri de siler.</span><span class="sxs-lookup"><span data-stu-id="71251-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="71251-108">İlişkili Azure depolama hesabında depolanan veriler silinmez.</span><span class="sxs-lookup"><span data-stu-id="71251-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="71251-109">Dış meta verileri 'nde depolanan veriler silinmez.</span><span class="sxs-lookup"><span data-stu-id="71251-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="71251-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71251-110">EXAMPLES</span></span>

### <span data-ttu-id="71251-111">Örnek 1: Azure HDInsight kümesini silme</span><span class="sxs-lookup"><span data-stu-id="71251-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="71251-112">Bu komut,-Hadoop-001 adlı kümeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="71251-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="71251-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71251-113">PARAMETERS</span></span>

### <span data-ttu-id="71251-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="71251-114">-ClusterName</span></span>
<span data-ttu-id="71251-115">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71251-115">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71251-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71251-116">-ResourceGroupName</span></span>
<span data-ttu-id="71251-117">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71251-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="71251-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71251-118">-DefaultProfile</span></span>
<span data-ttu-id="71251-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71251-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71251-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71251-120">CommonParameters</span></span>
<span data-ttu-id="71251-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71251-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71251-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71251-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71251-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71251-123">INPUTS</span></span>

## <span data-ttu-id="71251-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71251-124">OUTPUTS</span></span>

### <span data-ttu-id="71251-125">Microsoft. Azure. Management. HDInsight. model. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="71251-125">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="71251-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71251-126">NOTES</span></span>

## <span data-ttu-id="71251-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71251-127">RELATED LINKS</span></span>

[<span data-ttu-id="71251-128">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="71251-128">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="71251-129">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="71251-129">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


