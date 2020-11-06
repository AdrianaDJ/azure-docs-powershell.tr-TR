---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 93024e0719687c10ec07daa7269d742db012abe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594046"
---
# <span data-ttu-id="74266-101">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="74266-101">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="74266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74266-102">SYNOPSIS</span></span>
<span data-ttu-id="74266-103">Kümeye HTTP erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="74266-103">Disables HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74266-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74266-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74266-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="74266-105">DESCRIPTION</span></span>
<span data-ttu-id="74266-106">**Revoke-AzureRmHDInsightHttpServicesAccess** CMDLET 'i ODBC, ambarı, Oozie ve webHCatalog Web Services Için Azure HDıNSIGHT kümesine http erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="74266-106">The **Revoke-AzureRmHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="74266-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74266-107">EXAMPLES</span></span>

### <span data-ttu-id="74266-108">Örnek 1: kümeye HTTP erişimini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="74266-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="74266-109">Bu komut,-hadoop_001 adlı kümeye HTTP erişimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="74266-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="74266-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74266-110">PARAMETERS</span></span>

### <span data-ttu-id="74266-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="74266-111">-ClusterName</span></span>
<span data-ttu-id="74266-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74266-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="74266-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74266-113">-DefaultProfile</span></span>
<span data-ttu-id="74266-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="74266-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74266-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74266-115">-ResourceGroupName</span></span>
<span data-ttu-id="74266-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74266-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="74266-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74266-117">CommonParameters</span></span>
<span data-ttu-id="74266-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74266-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74266-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74266-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74266-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74266-120">INPUTS</span></span>

### <span data-ttu-id="74266-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="74266-121">None</span></span>

## <span data-ttu-id="74266-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74266-122">OUTPUTS</span></span>

### <span data-ttu-id="74266-123">Microsoft. Azure. Management. HDInsight. model. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="74266-123">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="74266-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74266-124">NOTES</span></span>

## <span data-ttu-id="74266-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74266-125">RELATED LINKS</span></span>

[<span data-ttu-id="74266-126">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="74266-126">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](./Grant-AzureRmHDInsightHttpServicesAccess.md)


