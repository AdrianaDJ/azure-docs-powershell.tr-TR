---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: e0f178c10fa74d8fa230472397d7bcc835f98bf4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280270"
---
# <span data-ttu-id="69b42-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="69b42-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="69b42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69b42-102">SYNOPSIS</span></span>
<span data-ttu-id="69b42-103">Bu IotHub 'in taşıyabileceği tüm geçerli SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="69b42-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="69b42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69b42-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69b42-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="69b42-105">DESCRIPTION</span></span>
<span data-ttu-id="69b42-106">Bu IotHub 'in taşıyabileceği tüm geçerli STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="69b42-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="69b42-107">IotHub, ücretsiz ve ücretli STB 'ler arasında geçiş yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="69b42-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="69b42-108">Bunu yapmak için iothub silmeli ve yeniden oluşturmalısınız.</span><span class="sxs-lookup"><span data-stu-id="69b42-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="69b42-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69b42-109">EXAMPLES</span></span>

### <span data-ttu-id="69b42-110">Örnek 1 geçerli STB 'leri alın</span><span class="sxs-lookup"><span data-stu-id="69b42-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="69b42-111">"Myiothub" adındaki IotHub için tüm SKU 'ların listesini alır</span><span class="sxs-lookup"><span data-stu-id="69b42-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="69b42-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69b42-112">PARAMETERS</span></span>

### <span data-ttu-id="69b42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b42-113">-DefaultProfile</span></span>
<span data-ttu-id="69b42-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="69b42-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69b42-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="69b42-115">-Name</span></span>
<span data-ttu-id="69b42-116">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="69b42-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="69b42-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69b42-117">-ResourceGroupName</span></span>
<span data-ttu-id="69b42-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="69b42-118">Resource Group Name</span></span>

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

### <span data-ttu-id="69b42-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b42-119">CommonParameters</span></span>
<span data-ttu-id="69b42-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69b42-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b42-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69b42-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b42-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69b42-122">INPUTS</span></span>

### <span data-ttu-id="69b42-123">System. String</span><span class="sxs-lookup"><span data-stu-id="69b42-123">System.String</span></span>

## <span data-ttu-id="69b42-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69b42-124">OUTPUTS</span></span>

### <span data-ttu-id="69b42-125">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubskudescription</span><span class="sxs-lookup"><span data-stu-id="69b42-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="69b42-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69b42-126">NOTES</span></span>

## <span data-ttu-id="69b42-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69b42-127">RELATED LINKS</span></span>
