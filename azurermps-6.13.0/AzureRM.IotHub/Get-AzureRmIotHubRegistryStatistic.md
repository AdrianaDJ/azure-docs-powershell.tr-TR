---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: a472ce25d648a70d9f47b6268b6bdf4f606f2a08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764390"
---
# <span data-ttu-id="b0345-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="b0345-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="b0345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0345-102">SYNOPSIS</span></span>
<span data-ttu-id="b0345-103">Bir IotHub için RegistryStatistics 'i alır.</span><span class="sxs-lookup"><span data-stu-id="b0345-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0345-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0345-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0345-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0345-105">DESCRIPTION</span></span>
<span data-ttu-id="b0345-106">Bir IotHub için RegistryStatistics 'i alır.</span><span class="sxs-lookup"><span data-stu-id="b0345-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="b0345-107">Bu, IotHub içindeki toplam etkin ve devre dışı aygıtların sayısı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="b0345-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="b0345-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0345-108">EXAMPLES</span></span>

### <span data-ttu-id="b0345-109">Örnek 1 RegistryStatistics 'i alma</span><span class="sxs-lookup"><span data-stu-id="b0345-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b0345-110">"Myiothub" adındaki IotHub için kayıt</span><span class="sxs-lookup"><span data-stu-id="b0345-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b0345-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0345-111">PARAMETERS</span></span>

### <span data-ttu-id="b0345-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0345-112">-DefaultProfile</span></span>
<span data-ttu-id="b0345-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b0345-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0345-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="b0345-114">-Name</span></span>
<span data-ttu-id="b0345-115">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="b0345-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="b0345-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0345-116">-ResourceGroupName</span></span>
<span data-ttu-id="b0345-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b0345-117">Resource Group Name</span></span>

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

### <span data-ttu-id="b0345-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0345-118">CommonParameters</span></span>
<span data-ttu-id="b0345-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0345-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0345-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0345-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0345-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0345-121">INPUTS</span></span>

### <span data-ttu-id="b0345-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b0345-122">System.String</span></span>

## <span data-ttu-id="b0345-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0345-123">OUTPUTS</span></span>

### <span data-ttu-id="b0345-124">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubregistrystatistics</span><span class="sxs-lookup"><span data-stu-id="b0345-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="b0345-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0345-125">NOTES</span></span>

## <span data-ttu-id="b0345-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0345-126">RELATED LINKS</span></span>
