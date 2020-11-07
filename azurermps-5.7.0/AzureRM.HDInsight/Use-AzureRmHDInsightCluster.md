---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/use-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: c8a58963e66c8260a0001c144230cabf3a80b295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764715"
---
# <span data-ttu-id="48919-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="48919-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="48919-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48919-102">SYNOPSIS</span></span>
<span data-ttu-id="48919-103">Invoke-RmAzureHDInsightHiveJob cmdlet 'inde kullanılacak kümeyi seçer.</span><span class="sxs-lookup"><span data-stu-id="48919-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48919-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48919-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48919-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48919-105">DESCRIPTION</span></span>
<span data-ttu-id="48919-106">**Use-AzureRmHDInsightCluster** cmdlet 'i, Invoke-AzureRmHDInsightHiveJob cmdlet 'Inin, kovan işlerini göndermek Için kullanacağı Azure HDInsight kümesini seçer.</span><span class="sxs-lookup"><span data-stu-id="48919-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="48919-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48919-107">EXAMPLES</span></span>

### <span data-ttu-id="48919-108">Örnek 1: yığın sorgu gönderimi için küme seçme</span><span class="sxs-lookup"><span data-stu-id="48919-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="48919-109">Bu komut, kovan sorgu gönderimi için bir küme seçer.</span><span class="sxs-lookup"><span data-stu-id="48919-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="48919-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48919-110">PARAMETERS</span></span>

### <span data-ttu-id="48919-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="48919-111">-ClusterName</span></span>
<span data-ttu-id="48919-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48919-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48919-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48919-113">-DefaultProfile</span></span>
<span data-ttu-id="48919-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="48919-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48919-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="48919-115">-HttpCredential</span></span>
<span data-ttu-id="48919-116">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="48919-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48919-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48919-117">-ResourceGroupName</span></span>
<span data-ttu-id="48919-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48919-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48919-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48919-119">CommonParameters</span></span>
<span data-ttu-id="48919-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48919-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48919-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48919-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48919-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48919-122">INPUTS</span></span>

### <span data-ttu-id="48919-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="48919-123">None</span></span>
<span data-ttu-id="48919-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="48919-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="48919-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48919-125">OUTPUTS</span></span>

### <span data-ttu-id="48919-126">System. String</span><span class="sxs-lookup"><span data-stu-id="48919-126">System.String</span></span>

## <span data-ttu-id="48919-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48919-127">NOTES</span></span>

## <span data-ttu-id="48919-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48919-128">RELATED LINKS</span></span>

[<span data-ttu-id="48919-129">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="48919-129">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="48919-130">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="48919-130">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


