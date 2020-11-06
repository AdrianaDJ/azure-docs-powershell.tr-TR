---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: 5f1e8037e4a9faef508c2ffd62ff00aca4387cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589140"
---
# <span data-ttu-id="2e74c-101">Get-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="2e74c-101">Get-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="2e74c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e74c-102">SYNOPSIS</span></span>
<span data-ttu-id="2e74c-103">Kaynak grubundaki belirtilen geçiş ad alanı için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="2e74c-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e74c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e74c-104">SYNTAX</span></span>

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e74c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e74c-105">DESCRIPTION</span></span>
<span data-ttu-id="2e74c-106">**Get-AzureRmRelayNamespace** cmdlet 'i, kaynak grubundaki belirtilen geçiş ad alanı için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="2e74c-106">The **Get-AzureRmRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="2e74c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e74c-107">EXAMPLES</span></span>

### <span data-ttu-id="2e74c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2e74c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="2e74c-109">Belirtilen geçiş ad alanının açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="2e74c-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="2e74c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e74c-110">PARAMETERS</span></span>

### <span data-ttu-id="2e74c-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e74c-111">-Name</span></span>
<span data-ttu-id="2e74c-112">Geçiş ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="2e74c-112">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e74c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e74c-113">-ResourceGroupName</span></span>
<span data-ttu-id="2e74c-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2e74c-114">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e74c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e74c-115">-DefaultProfile</span></span>
<span data-ttu-id="2e74c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e74c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e74c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e74c-117">CommonParameters</span></span>
<span data-ttu-id="2e74c-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e74c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e74c-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e74c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e74c-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e74c-120">INPUTS</span></span>

### <span data-ttu-id="2e74c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e74c-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e74c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="2e74c-122">System.String</span></span>

### <span data-ttu-id="2e74c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e74c-123">-Name</span></span>
 <span data-ttu-id="2e74c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2e74c-124">System.String</span></span>

## <span data-ttu-id="2e74c-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e74c-125">OUTPUTS</span></span>

### <span data-ttu-id="2e74c-126">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Relay. modeller. RelayNamespaceAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2e74c-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="2e74c-127">ProvisioningState: başarılı CreatedAt: 4/12/2017 12:38:47 har UpdatedAt: 4/12/2017 12:39:10 Öservicebusendpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ metricid: 854d368f-1828-428f-8f3c-f2affa9b2f7d: TestNamespace-Relay1 location: West US Etiketler: {[Tag1, Tag1Value]} ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 adı: TestNameSpace-Relay1 tür: Microsoft. Relay/Namespaces</span><span class="sxs-lookup"><span data-stu-id="2e74c-127">ProvisioningState  : Succeeded CreatedAt          : 4/12/2017 12:38:47 AM UpdatedAt          : 4/12/2017 12:39:10 AM ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1 Location           : West US Tags               : {[tag1, Tag1Value]} Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 Name               : TestNameSpace-Relay1 Type               : Microsoft.Relay/namespaces</span></span>

## <span data-ttu-id="2e74c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e74c-128">NOTES</span></span>

## <span data-ttu-id="2e74c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e74c-129">RELATED LINKS</span></span>

