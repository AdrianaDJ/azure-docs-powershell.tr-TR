---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 09b389763897f91a23f56f0a3383dd3f7f03ca1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762372"
---
# <span data-ttu-id="e1ce9-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e1ce9-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="e1ce9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ce9-103">Windows kümesine RDP erişimi verir.</span><span class="sxs-lookup"><span data-stu-id="e1ce9-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1ce9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1ce9-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1ce9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1ce9-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ce9-106">**Grant-AzureRmHDInsightRdpServicesAccess** cmdlet 'ı, Uzak Masaüstü Protokolü 'NÜN (RDP) Windows tabanlı bir Azure HDInsight kümesine erişmesini olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="e1ce9-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e1ce9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1ce9-107">EXAMPLES</span></span>

### <span data-ttu-id="e1ce9-108">Örnek 1: Azure HDInsight kümesine RDP erişimi verme</span><span class="sxs-lookup"><span data-stu-id="e1ce9-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="e1ce9-109">Bu komut,-Hadoop-001 adlı kümeye RDP erişimi verir.</span><span class="sxs-lookup"><span data-stu-id="e1ce9-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e1ce9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1ce9-110">PARAMETERS</span></span>

### <span data-ttu-id="e1ce9-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e1ce9-111">-ClusterName</span></span>
<span data-ttu-id="e1ce9-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1ce9-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e1ce9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ce9-113">-DefaultProfile</span></span>
<span data-ttu-id="e1ce9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e1ce9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1ce9-115">-Rdpaccessexpme</span><span class="sxs-lookup"><span data-stu-id="e1ce9-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="e1ce9-116">Bir kümeye RDP erişimi için **Tarih saat** sonu</span><span class="sxs-lookup"><span data-stu-id="e1ce9-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ce9-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="e1ce9-117">-RdpCredential</span></span>
<span data-ttu-id="e1ce9-118">Kümenin RDP kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1ce9-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="e1ce9-119">Bu yalnızca Windows kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="e1ce9-119">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="e1ce9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ce9-120">-ResourceGroupName</span></span>
<span data-ttu-id="e1ce9-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1ce9-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e1ce9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ce9-122">CommonParameters</span></span>
<span data-ttu-id="e1ce9-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1ce9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ce9-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ce9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ce9-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1ce9-125">INPUTS</span></span>

### <span data-ttu-id="e1ce9-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e1ce9-126">None</span></span>
<span data-ttu-id="e1ce9-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e1ce9-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1ce9-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1ce9-128">OUTPUTS</span></span>

### <span data-ttu-id="e1ce9-129">System. void</span><span class="sxs-lookup"><span data-stu-id="e1ce9-129">System.Void</span></span>

## <span data-ttu-id="e1ce9-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1ce9-130">NOTES</span></span>

## <span data-ttu-id="e1ce9-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1ce9-131">RELATED LINKS</span></span>

[<span data-ttu-id="e1ce9-132">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e1ce9-132">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


