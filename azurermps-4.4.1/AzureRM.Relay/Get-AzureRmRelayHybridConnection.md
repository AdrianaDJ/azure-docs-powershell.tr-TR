---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 2fccb11ba45fa1d532c35140db588294895c0802
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589141"
---
# <span data-ttu-id="19490-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="19490-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="19490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19490-102">SYNOPSIS</span></span>
<span data-ttu-id="19490-103">Geçiş ad alanında belirtilen HybridConnection için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="19490-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19490-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19490-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19490-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19490-105">DESCRIPTION</span></span>
<span data-ttu-id="19490-106">**Get-AzureRmRelayHybridConnection** cmdlet 'ı, geçiş ad alanında belirtilen HybridConnection için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="19490-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="19490-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19490-107">EXAMPLES</span></span>

### <span data-ttu-id="19490-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="19490-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="19490-109">HybridConnection 'un açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="19490-109">Returns the description of the HybridConnection.</span></span> 

## <span data-ttu-id="19490-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19490-110">PARAMETERS</span></span>

### <span data-ttu-id="19490-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="19490-111">-Name</span></span>
<span data-ttu-id="19490-112">HybridConnections adı.</span><span class="sxs-lookup"><span data-stu-id="19490-112">HybridConnections Name.</span></span>

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

### <span data-ttu-id="19490-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="19490-113">-Namespace</span></span>
<span data-ttu-id="19490-114">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="19490-114">Namespace Name.</span></span>

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

### <span data-ttu-id="19490-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19490-115">-ResourceGroupName</span></span>
<span data-ttu-id="19490-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="19490-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="19490-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19490-117">-DefaultProfile</span></span>
<span data-ttu-id="19490-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19490-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19490-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19490-119">CommonParameters</span></span>
<span data-ttu-id="19490-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19490-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19490-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19490-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19490-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19490-122">INPUTS</span></span>

### <span data-ttu-id="19490-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19490-123">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="19490-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="19490-124">-Namespace</span></span>
    System.String

### <span data-ttu-id="19490-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="19490-125">-Name</span></span>
    System.String

## <span data-ttu-id="19490-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19490-126">OUTPUTS</span></span>

### <span data-ttu-id="19490-127">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Relay. modeller. HybridConnectionAttibutes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="19490-127">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="19490-128">CreatedAt: 4/12/2017 3:17:02 Öupdatedat: 4/12/2017 3:17:02 har ListenerCount: 0 Requiresclientauthor,: true UserMetadata: Kullanıcı meta veri kimliği:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name: TestHybridConnection Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="19490-128">CreatedAt                   : 4/12/2017 3:17:02 AM UpdatedAt                   : 4/12/2017 3:17:02 AM ListenerCount               : 0 RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name                        : TestHybridConnection Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="19490-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19490-129">NOTES</span></span>

## <span data-ttu-id="19490-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19490-130">RELATED LINKS</span></span>

