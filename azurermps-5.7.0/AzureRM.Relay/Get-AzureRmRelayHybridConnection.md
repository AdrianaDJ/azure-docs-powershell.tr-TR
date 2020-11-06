---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 08a20958975d78a945e3e73729d5841f6dda6811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592417"
---
# <span data-ttu-id="2b10e-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="2b10e-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="2b10e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b10e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b10e-103">Geçiş ad alanında belirtilen HybridConnection için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="2b10e-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b10e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b10e-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b10e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b10e-105">DESCRIPTION</span></span>
<span data-ttu-id="2b10e-106">**Get-AzureRmRelayHybridConnection** cmdlet 'ı, geçiş ad alanında belirtilen HybridConnection için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="2b10e-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="2b10e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b10e-107">EXAMPLES</span></span>

### <span data-ttu-id="2b10e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2b10e-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="2b10e-109">HybridConnection 'un açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="2b10e-109">Returns the description of the HybridConnection.</span></span> 

## <span data-ttu-id="2b10e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b10e-110">PARAMETERS</span></span>

### <span data-ttu-id="2b10e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b10e-111">-DefaultProfile</span></span>
<span data-ttu-id="2b10e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b10e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b10e-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b10e-113">-Name</span></span>
<span data-ttu-id="2b10e-114">HybridConnections adı.</span><span class="sxs-lookup"><span data-stu-id="2b10e-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="2b10e-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2b10e-115">-Namespace</span></span>
<span data-ttu-id="2b10e-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="2b10e-116">Namespace Name.</span></span>

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

### <span data-ttu-id="2b10e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b10e-117">-ResourceGroupName</span></span>
<span data-ttu-id="2b10e-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2b10e-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="2b10e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b10e-119">CommonParameters</span></span>
<span data-ttu-id="2b10e-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b10e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b10e-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b10e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b10e-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b10e-122">INPUTS</span></span>

### <span data-ttu-id="2b10e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b10e-123">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="2b10e-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2b10e-124">-Namespace</span></span>
    System.String

### <span data-ttu-id="2b10e-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b10e-125">-Name</span></span>
    System.String

## <span data-ttu-id="2b10e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b10e-126">OUTPUTS</span></span>

### <span data-ttu-id="2b10e-127">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Relay. modeller. HybridConnectionAttibutes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2b10e-127">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="2b10e-128">CreatedAt: 4/12/2017 3:17:02 Öupdatedat: 4/12/2017 3:17:02 har ListenerCount: 0 Requiresclientauthor,: true UserMetadata: Kullanıcı meta veri kimliği:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name: TestHybridConnection Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="2b10e-128">CreatedAt                   : 4/12/2017 3:17:02 AM UpdatedAt                   : 4/12/2017 3:17:02 AM ListenerCount               : 0 RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name                        : TestHybridConnection Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="2b10e-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b10e-129">NOTES</span></span>

## <span data-ttu-id="2b10e-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b10e-130">RELATED LINKS</span></span>

