---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
ms.openlocfilehash: 904fb627be4460fbbca0dc6dae9a68fc0dd468ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594269"
---
# <span data-ttu-id="4261f-101">Get-AzureRmIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="4261f-101">Get-AzureRmIotHubValidSku</span></span>

## <span data-ttu-id="4261f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4261f-102">SYNOPSIS</span></span>
<span data-ttu-id="4261f-103">Bu IotHub 'in taşıyabileceği tüm geçerli SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="4261f-103">Gets all valid skus that this IotHub can transition to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4261f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4261f-104">SYNTAX</span></span>

```
Get-AzureRmIotHubValidSku [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4261f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4261f-105">DESCRIPTION</span></span>
<span data-ttu-id="4261f-106">Bu IotHub 'in taşıyabileceği tüm geçerli STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="4261f-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="4261f-107">IotHub, ücretsiz ve ücretli STB 'ler arasında geçiş yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="4261f-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="4261f-108">Bunu yapmak için iothub silmeli ve yeniden oluşturmalısınız.</span><span class="sxs-lookup"><span data-stu-id="4261f-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="4261f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4261f-109">EXAMPLES</span></span>

### <span data-ttu-id="4261f-110">Örnek 1 geçerli STB 'leri alın</span><span class="sxs-lookup"><span data-stu-id="4261f-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzureRmIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4261f-111">"Myiothub" adındaki IotHub için tüm SKU 'ların listesini alır</span><span class="sxs-lookup"><span data-stu-id="4261f-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="4261f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4261f-112">PARAMETERS</span></span>

### <span data-ttu-id="4261f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="4261f-113">-Name</span></span>
<span data-ttu-id="4261f-114">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="4261f-114">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4261f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4261f-115">-ResourceGroupName</span></span>
<span data-ttu-id="4261f-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4261f-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4261f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4261f-117">-DefaultProfile</span></span>
<span data-ttu-id="4261f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4261f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4261f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4261f-119">CommonParameters</span></span>
<span data-ttu-id="4261f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4261f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4261f-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4261f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4261f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4261f-122">INPUTS</span></span>

### <span data-ttu-id="4261f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4261f-123">System.String</span></span>

## <span data-ttu-id="4261f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4261f-124">OUTPUTS</span></span>

### <span data-ttu-id="4261f-125">System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubskudescription, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4261f-125">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4261f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4261f-126">NOTES</span></span>

## <span data-ttu-id="4261f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4261f-127">RELATED LINKS</span></span>

