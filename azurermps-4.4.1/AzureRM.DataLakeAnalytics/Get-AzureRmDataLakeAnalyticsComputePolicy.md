---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 59bc611d63d062d06b3b3bdebe9ac8b0f1349179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764867"
---
# <span data-ttu-id="e931e-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="e931e-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="e931e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e931e-102">SYNOPSIS</span></span>
<span data-ttu-id="e931e-103">Bir Data Lake Analytics COMPUTE ilkesi veya compute ilkeleri listesi alır.</span><span class="sxs-lookup"><span data-stu-id="e931e-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e931e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e931e-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e931e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e931e-105">DESCRIPTION</span></span>
<span data-ttu-id="e931e-106">**Get-AzureRmDataLakeAnalyticsComputePolicy** , belirtilen bir Azure Data Lake Analytics COMPUTE ilkesi veya ilkelerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="e931e-106">The **Get-AzureRmDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="e931e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e931e-107">EXAMPLES</span></span>

### <span data-ttu-id="e931e-108">Örnek 1: belirli bir işlem ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="e931e-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="e931e-109">Bu komut, ' contosoadla ' hesabında ' myPolicy ' adlı belirtilen hesaplama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="e931e-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="e931e-110">Örnek 2: hesapta tüm işlem ilkelerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="e931e-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="e931e-111">Bu komut, "contosoadla" hesabındaki tüm işlem ilkelerinin listesini alır</span><span class="sxs-lookup"><span data-stu-id="e931e-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="e931e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e931e-112">PARAMETERS</span></span>

### <span data-ttu-id="e931e-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="e931e-113">-Account</span></span>
<span data-ttu-id="e931e-114">İşlem ilkesinin veya ilkelerin alınacağı hesabın adı.</span><span class="sxs-lookup"><span data-stu-id="e931e-114">Name of the account to get the compute policy or policies from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e931e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e931e-115">-Name</span></span>
<span data-ttu-id="e931e-116">Alınacak işlem ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="e931e-116">Name of the compute policy to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e931e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e931e-117">-ResourceGroupName</span></span>
<span data-ttu-id="e931e-118">Hesabınızın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e931e-118">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="e931e-119">İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="e931e-119">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="e931e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e931e-120">-DefaultProfile</span></span>
<span data-ttu-id="e931e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e931e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e931e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e931e-122">CommonParameters</span></span>
<span data-ttu-id="e931e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e931e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e931e-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e931e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e931e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e931e-125">INPUTS</span></span>

### <span data-ttu-id="e931e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e931e-126">System.String</span></span>

## <span data-ttu-id="e931e-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e931e-127">OUTPUTS</span></span>

### <span data-ttu-id="e931e-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="e931e-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>
<span data-ttu-id="e931e-129">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft. Azure. Commands. DataLakeAnalytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e931e-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft.Azure.Commands.DataLakeAnalytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e931e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e931e-130">NOTES</span></span>

## <span data-ttu-id="e931e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e931e-131">RELATED LINKS</span></span>

