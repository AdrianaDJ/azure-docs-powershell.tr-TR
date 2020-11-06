---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 88d2c8f7b0bcab3faad6368070606b8a36948343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593450"
---
# <span data-ttu-id="6a1a6-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="6a1a6-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="6a1a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a1a6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a1a6-103">Belirtilen WcfRelay için bir açıklama döndürür.</span><span class="sxs-lookup"><span data-stu-id="6a1a6-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a1a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a1a6-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a1a6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a1a6-105">DESCRIPTION</span></span>
<span data-ttu-id="6a1a6-106">**Get-AzureRmWcfRelay** cmdlet 'ı belirtilen wcfrelay 'in açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="6a1a6-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="6a1a6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a1a6-107">EXAMPLES</span></span>

### <span data-ttu-id="6a1a6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6a1a6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="6a1a6-109">WcfRelay 'in açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="6a1a6-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="6a1a6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a1a6-110">PARAMETERS</span></span>

### <span data-ttu-id="6a1a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a1a6-111">-DefaultProfile</span></span>
<span data-ttu-id="6a1a6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a1a6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a1a6-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a1a6-113">-Name</span></span>
<span data-ttu-id="6a1a6-114">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="6a1a6-114">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a1a6-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6a1a6-115">-Namespace</span></span>
<span data-ttu-id="6a1a6-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="6a1a6-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a1a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a1a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="6a1a6-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6a1a6-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a1a6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a1a6-119">CommonParameters</span></span>
<span data-ttu-id="6a1a6-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a1a6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a1a6-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a1a6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a1a6-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a1a6-122">INPUTS</span></span>

### <span data-ttu-id="6a1a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a1a6-123">-ResourceGroupName</span></span>
 <span data-ttu-id="6a1a6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6a1a6-124">System.String</span></span>
 

### <span data-ttu-id="6a1a6-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6a1a6-125">-Namespace</span></span>
 <span data-ttu-id="6a1a6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6a1a6-126">System.String</span></span>
 

### <span data-ttu-id="6a1a6-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a1a6-127">-Name</span></span>
 <span data-ttu-id="6a1a6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6a1a6-128">System.String</span></span> 

## <span data-ttu-id="6a1a6-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a1a6-129">OUTPUTS</span></span>

### <span data-ttu-id="6a1a6-130">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Relay. modeller. WcfRelayAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6a1a6-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="6a1a6-131">RelayType: NetTcp createdat: 4/12/2017 2:23:08 ısupdatedat: 4/12/2017 2:23:08 övsayı: 0 requiresclientauthorleme: doğru requirestransportsecurıty: doğru IsDynamic: false usermetadata: Kullanıcı meta veri kimliği:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfreroa/TestWCFRelay1 Name: TestWCFRelay1 tür: Microsoft. Relay/wcfreroa</span><span class="sxs-lookup"><span data-stu-id="6a1a6-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="6a1a6-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a1a6-132">NOTES</span></span>

## <span data-ttu-id="6a1a6-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a1a6-133">RELATED LINKS</span></span>

