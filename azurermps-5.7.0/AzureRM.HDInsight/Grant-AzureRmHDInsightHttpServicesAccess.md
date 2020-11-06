---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 529eedf9cd8ae782d08af7d349d4e11885a8a564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588210"
---
# <span data-ttu-id="58362-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="58362-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="58362-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58362-102">SYNOPSIS</span></span>
<span data-ttu-id="58362-103">Kümeye HTTP erişimi verir.</span><span class="sxs-lookup"><span data-stu-id="58362-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58362-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58362-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58362-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="58362-105">DESCRIPTION</span></span>
<span data-ttu-id="58362-106">**Grant-AzureRmHDInsightHttpServicesAccess** cmdlet 'ı, ODBC, ambarı, Oozie ve Web Hizmetleri kullanarak bir Azure HDıNSIGHT kümesine http erişimi verir.</span><span class="sxs-lookup"><span data-stu-id="58362-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="58362-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58362-107">EXAMPLES</span></span>

### <span data-ttu-id="58362-108">Örnek 1: Azure HDInsight kümesine HTTP erişimi verme</span><span class="sxs-lookup"><span data-stu-id="58362-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="58362-109">Bu komut,-Hadoop-001 adlı kümeye HTTP erişimi verir.</span><span class="sxs-lookup"><span data-stu-id="58362-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="58362-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58362-110">PARAMETERS</span></span>

### <span data-ttu-id="58362-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="58362-111">-ClusterName</span></span>
<span data-ttu-id="58362-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58362-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="58362-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58362-113">-DefaultProfile</span></span>
<span data-ttu-id="58362-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="58362-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58362-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="58362-115">-HttpCredential</span></span>
<span data-ttu-id="58362-116">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="58362-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58362-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58362-117">-ResourceGroupName</span></span>
<span data-ttu-id="58362-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58362-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="58362-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58362-119">CommonParameters</span></span>
<span data-ttu-id="58362-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58362-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58362-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58362-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58362-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58362-122">INPUTS</span></span>

### <span data-ttu-id="58362-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="58362-123">None</span></span>
<span data-ttu-id="58362-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="58362-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="58362-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58362-125">OUTPUTS</span></span>

### <span data-ttu-id="58362-126">Microsoft. Azure. Management. HDInsight. model. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="58362-126">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="58362-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58362-127">NOTES</span></span>

## <span data-ttu-id="58362-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58362-128">RELATED LINKS</span></span>

[<span data-ttu-id="58362-129">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="58362-129">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)


