---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: f19c4f9d39837534ea5ddd5b16daa055ee54aef6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589829"
---
# <span data-ttu-id="2c723-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="2c723-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="2c723-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c723-102">SYNOPSIS</span></span>
<span data-ttu-id="2c723-103">Bir Data Lake Analytics COMPUTE ilkesi veya compute ilkeleri listesi alır.</span><span class="sxs-lookup"><span data-stu-id="2c723-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c723-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c723-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c723-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c723-105">DESCRIPTION</span></span>
<span data-ttu-id="2c723-106">**Get-AzureRmDataLakeAnalyticsComputePolicy** , belirtilen bir Azure Data Lake Analytics COMPUTE ilkesi veya ilkelerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="2c723-106">The **Get-AzureRmDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="2c723-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c723-107">EXAMPLES</span></span>

### <span data-ttu-id="2c723-108">Örnek 1: belirli bir işlem ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="2c723-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="2c723-109">Bu komut, ' contosoadla ' hesabında ' myPolicy ' adlı belirtilen hesaplama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="2c723-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="2c723-110">Örnek 2: hesapta tüm işlem ilkelerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="2c723-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="2c723-111">Bu komut, "contosoadla" hesabındaki tüm işlem ilkelerinin listesini alır</span><span class="sxs-lookup"><span data-stu-id="2c723-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="2c723-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c723-112">PARAMETERS</span></span>

### <span data-ttu-id="2c723-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="2c723-113">-Account</span></span>
<span data-ttu-id="2c723-114">İşlem ilkesinin veya ilkelerin alınacağı hesabın adı.</span><span class="sxs-lookup"><span data-stu-id="2c723-114">Name of the account to get the compute policy or policies from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c723-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c723-115">-DefaultProfile</span></span>
<span data-ttu-id="2c723-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2c723-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c723-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c723-117">-Name</span></span>
<span data-ttu-id="2c723-118">Alınacak işlem ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="2c723-118">Name of the compute policy to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c723-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c723-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c723-120">Hesabınızın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2c723-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="2c723-121">İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="2c723-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="2c723-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c723-122">CommonParameters</span></span>
<span data-ttu-id="2c723-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c723-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c723-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c723-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c723-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c723-125">INPUTS</span></span>

### <span data-ttu-id="2c723-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2c723-126">System.String</span></span>

## <span data-ttu-id="2c723-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c723-127">OUTPUTS</span></span>

### <span data-ttu-id="2c723-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="2c723-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>
<span data-ttu-id="2c723-129">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft. Azure. Commands. DataLakeAnalytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2c723-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft.Azure.Commands.DataLakeAnalytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2c723-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c723-130">NOTES</span></span>

## <span data-ttu-id="2c723-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c723-131">RELATED LINKS</span></span>

