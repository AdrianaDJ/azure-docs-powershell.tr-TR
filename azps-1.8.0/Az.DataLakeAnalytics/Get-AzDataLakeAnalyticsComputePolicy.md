---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 776249a7a474e3918ed29003f631c984111ca25c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761101"
---
# <span data-ttu-id="f5785-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="f5785-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="f5785-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5785-102">SYNOPSIS</span></span>
<span data-ttu-id="f5785-103">Bir Data Lake Analytics COMPUTE ilkesi veya compute ilkeleri listesi alır.</span><span class="sxs-lookup"><span data-stu-id="f5785-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="f5785-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5785-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5785-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5785-105">DESCRIPTION</span></span>
<span data-ttu-id="f5785-106">**Get-AzDataLakeAnalyticsComputePolicy** , belirtilen bir Azure Data Lake Analytics COMPUTE ilkesi veya ilkelerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="f5785-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="f5785-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5785-107">EXAMPLES</span></span>

### <span data-ttu-id="f5785-108">Örnek 1: belirli bir işlem ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="f5785-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="f5785-109">Bu komut, ' contosoadla ' hesabında ' myPolicy ' adlı belirtilen hesaplama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="f5785-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="f5785-110">Örnek 2: hesapta tüm işlem ilkelerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="f5785-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="f5785-111">Bu komut, "contosoadla" hesabındaki tüm işlem ilkelerinin listesini alır</span><span class="sxs-lookup"><span data-stu-id="f5785-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="f5785-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5785-112">PARAMETERS</span></span>

### <span data-ttu-id="f5785-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="f5785-113">-Account</span></span>
<span data-ttu-id="f5785-114">İşlem ilkesinin veya ilkelerin alınacağı hesabın adı.</span><span class="sxs-lookup"><span data-stu-id="f5785-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="f5785-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5785-115">-DefaultProfile</span></span>
<span data-ttu-id="f5785-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f5785-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5785-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5785-117">-Name</span></span>
<span data-ttu-id="f5785-118">Alınacak işlem ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="f5785-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="f5785-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5785-119">-ResourceGroupName</span></span>
<span data-ttu-id="f5785-120">Hesabınızın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f5785-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="f5785-121">İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="f5785-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="f5785-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5785-122">CommonParameters</span></span>
<span data-ttu-id="f5785-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5785-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5785-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5785-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5785-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5785-125">INPUTS</span></span>

### <span data-ttu-id="f5785-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f5785-126">System.String</span></span>

## <span data-ttu-id="f5785-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5785-127">OUTPUTS</span></span>

### <span data-ttu-id="f5785-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="f5785-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="f5785-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5785-129">NOTES</span></span>

## <span data-ttu-id="f5785-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5785-130">RELATED LINKS</span></span>
