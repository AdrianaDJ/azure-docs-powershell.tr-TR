---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
ms.openlocfilehash: d1c52cef6548f8762f972789a1fd9d47e8cc92aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764386"
---
# <span data-ttu-id="57fe6-101">Get-AzureRmIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="57fe6-101">Get-AzureRmIotHubValidSku</span></span>

## <span data-ttu-id="57fe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="57fe6-103">Bu IotHub 'in taşıyabileceği tüm geçerli SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="57fe6-103">Gets all valid skus that this IotHub can transition to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57fe6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57fe6-104">SYNTAX</span></span>

```
Get-AzureRmIotHubValidSku [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57fe6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="57fe6-105">DESCRIPTION</span></span>
<span data-ttu-id="57fe6-106">Bu IotHub 'in taşıyabileceği tüm geçerli STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="57fe6-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="57fe6-107">IotHub, ücretsiz ve ücretli STB 'ler arasında geçiş yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="57fe6-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="57fe6-108">Bunu yapmak için iothub silmeli ve yeniden oluşturmalısınız.</span><span class="sxs-lookup"><span data-stu-id="57fe6-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="57fe6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57fe6-109">EXAMPLES</span></span>

### <span data-ttu-id="57fe6-110">Örnek 1 geçerli STB 'leri alın</span><span class="sxs-lookup"><span data-stu-id="57fe6-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzureRmIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="57fe6-111">"Myiothub" adındaki IotHub için tüm SKU 'ların listesini alır</span><span class="sxs-lookup"><span data-stu-id="57fe6-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="57fe6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57fe6-112">PARAMETERS</span></span>

### <span data-ttu-id="57fe6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57fe6-113">-DefaultProfile</span></span>
<span data-ttu-id="57fe6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="57fe6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57fe6-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="57fe6-115">-Name</span></span>
<span data-ttu-id="57fe6-116">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="57fe6-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="57fe6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57fe6-117">-ResourceGroupName</span></span>
<span data-ttu-id="57fe6-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="57fe6-118">Resource Group Name</span></span>

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

### <span data-ttu-id="57fe6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57fe6-119">CommonParameters</span></span>
<span data-ttu-id="57fe6-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57fe6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57fe6-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57fe6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57fe6-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57fe6-122">INPUTS</span></span>

### <span data-ttu-id="57fe6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="57fe6-123">System.String</span></span>

## <span data-ttu-id="57fe6-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57fe6-124">OUTPUTS</span></span>

### <span data-ttu-id="57fe6-125">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubskudescription</span><span class="sxs-lookup"><span data-stu-id="57fe6-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="57fe6-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57fe6-126">NOTES</span></span>

## <span data-ttu-id="57fe6-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57fe6-127">RELATED LINKS</span></span>
