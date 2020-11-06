---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 8c3fd2340c1e15d5229a5fdfe9331b1d31c8c02a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594045"
---
# <span data-ttu-id="304ac-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="304ac-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="304ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="304ac-102">SYNOPSIS</span></span>
<span data-ttu-id="304ac-103">Windows kümesine RDP erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="304ac-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="304ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="304ac-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="304ac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="304ac-105">DESCRIPTION</span></span>
<span data-ttu-id="304ac-106">**Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet 'i Windows tabanlı bir Azure HDInsight kümesine Uzak Masaüstü Protokolü (RDP) erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="304ac-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="304ac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="304ac-107">EXAMPLES</span></span>

### <span data-ttu-id="304ac-108">Örnek 1: belirtilen kümeye RDP erişimini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="304ac-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="304ac-109">Bu komut,-Hadoop-001 adlı kümeye RDP erişimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="304ac-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="304ac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="304ac-110">PARAMETERS</span></span>

### <span data-ttu-id="304ac-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="304ac-111">-ClusterName</span></span>
<span data-ttu-id="304ac-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="304ac-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="304ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="304ac-113">-DefaultProfile</span></span>
<span data-ttu-id="304ac-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="304ac-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="304ac-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="304ac-115">-ResourceGroupName</span></span>
<span data-ttu-id="304ac-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="304ac-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="304ac-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304ac-117">CommonParameters</span></span>
<span data-ttu-id="304ac-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="304ac-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304ac-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="304ac-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304ac-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="304ac-120">INPUTS</span></span>

### <span data-ttu-id="304ac-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="304ac-121">None</span></span>

## <span data-ttu-id="304ac-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="304ac-122">OUTPUTS</span></span>

### <span data-ttu-id="304ac-123">System. void</span><span class="sxs-lookup"><span data-stu-id="304ac-123">System.Void</span></span>

## <span data-ttu-id="304ac-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="304ac-124">NOTES</span></span>

## <span data-ttu-id="304ac-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="304ac-125">RELATED LINKS</span></span>

[<span data-ttu-id="304ac-126">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="304ac-126">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)


