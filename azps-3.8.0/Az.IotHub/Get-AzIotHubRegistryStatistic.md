---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103825"
---
# <span data-ttu-id="cbdda-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="cbdda-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="cbdda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbdda-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdda-103">Bir IotHub için RegistryStatistics 'i alır.</span><span class="sxs-lookup"><span data-stu-id="cbdda-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="cbdda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cbdda-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbdda-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cbdda-105">DESCRIPTION</span></span>
<span data-ttu-id="cbdda-106">Bir IotHub için RegistryStatistics 'i alır.</span><span class="sxs-lookup"><span data-stu-id="cbdda-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="cbdda-107">Bu, IotHub içindeki toplam etkin ve devre dışı aygıtların sayısı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="cbdda-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="cbdda-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cbdda-108">EXAMPLES</span></span>

### <span data-ttu-id="cbdda-109">Örnek 1 RegistryStatistics 'i alma</span><span class="sxs-lookup"><span data-stu-id="cbdda-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="cbdda-110">"Myiothub" adındaki IotHub için kayıt</span><span class="sxs-lookup"><span data-stu-id="cbdda-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="cbdda-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cbdda-111">PARAMETERS</span></span>

### <span data-ttu-id="cbdda-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdda-112">-DefaultProfile</span></span>
<span data-ttu-id="cbdda-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cbdda-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbdda-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="cbdda-114">-Name</span></span>
<span data-ttu-id="cbdda-115">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="cbdda-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="cbdda-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbdda-116">-ResourceGroupName</span></span>
<span data-ttu-id="cbdda-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cbdda-117">Resource Group Name</span></span>

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

### <span data-ttu-id="cbdda-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdda-118">CommonParameters</span></span>
<span data-ttu-id="cbdda-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cbdda-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdda-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbdda-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdda-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cbdda-121">INPUTS</span></span>

### <span data-ttu-id="cbdda-122">System. String</span><span class="sxs-lookup"><span data-stu-id="cbdda-122">System.String</span></span>

## <span data-ttu-id="cbdda-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cbdda-123">OUTPUTS</span></span>

### <span data-ttu-id="cbdda-124">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubregistrystatistics</span><span class="sxs-lookup"><span data-stu-id="cbdda-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="cbdda-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cbdda-125">NOTES</span></span>

## <span data-ttu-id="cbdda-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cbdda-126">RELATED LINKS</span></span>
