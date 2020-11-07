---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: bb4ab11406a644d34bdb5b45ea3b3fba47376826
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916456"
---
# <span data-ttu-id="4147b-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="4147b-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="4147b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4147b-102">SYNOPSIS</span></span>
<span data-ttu-id="4147b-103">Bir IotHub için RegistryStatistics 'i alır.</span><span class="sxs-lookup"><span data-stu-id="4147b-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="4147b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4147b-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4147b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4147b-105">DESCRIPTION</span></span>
<span data-ttu-id="4147b-106">Bir IotHub için RegistryStatistics 'i alır.</span><span class="sxs-lookup"><span data-stu-id="4147b-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="4147b-107">Bu, IotHub içindeki toplam etkin ve devre dışı aygıtların sayısı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="4147b-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="4147b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4147b-108">EXAMPLES</span></span>

### <span data-ttu-id="4147b-109">Örnek 1 RegistryStatistics 'i alma</span><span class="sxs-lookup"><span data-stu-id="4147b-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4147b-110">"Myiothub" adındaki IotHub için kayıt</span><span class="sxs-lookup"><span data-stu-id="4147b-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="4147b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4147b-111">PARAMETERS</span></span>

### <span data-ttu-id="4147b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4147b-112">-DefaultProfile</span></span>
<span data-ttu-id="4147b-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4147b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4147b-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="4147b-114">-Name</span></span>
<span data-ttu-id="4147b-115">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="4147b-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="4147b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4147b-116">-ResourceGroupName</span></span>
<span data-ttu-id="4147b-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4147b-117">Resource Group Name</span></span>

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

### <span data-ttu-id="4147b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4147b-118">CommonParameters</span></span>
<span data-ttu-id="4147b-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4147b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4147b-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4147b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4147b-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4147b-121">INPUTS</span></span>

### <span data-ttu-id="4147b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="4147b-122">System.String</span></span>

## <span data-ttu-id="4147b-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4147b-123">OUTPUTS</span></span>

### <span data-ttu-id="4147b-124">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubregistrystatistics</span><span class="sxs-lookup"><span data-stu-id="4147b-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="4147b-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4147b-125">NOTES</span></span>

## <span data-ttu-id="4147b-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4147b-126">RELATED LINKS</span></span>