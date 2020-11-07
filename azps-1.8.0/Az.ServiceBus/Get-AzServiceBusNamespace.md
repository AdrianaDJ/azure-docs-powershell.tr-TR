---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: 1e4e1d50df44715fe433a5106619264063b2f22e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759201"
---
# <span data-ttu-id="d84f2-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="d84f2-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="d84f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d84f2-102">SYNOPSIS</span></span>
<span data-ttu-id="d84f2-103">Kaynak grubunda belirtilen Service Bus ad alanı için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="d84f2-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="d84f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d84f2-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d84f2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d84f2-105">DESCRIPTION</span></span>
<span data-ttu-id="d84f2-106">**Get-AzServiceBusNamespace** cmdlet 'i, kaynak grubundaki belirtilen Service Bus ad alanı için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="d84f2-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="d84f2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d84f2-107">EXAMPLES</span></span>

### <span data-ttu-id="d84f2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d84f2-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="d84f2-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d84f2-109">PARAMETERS</span></span>

### <span data-ttu-id="d84f2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84f2-110">-DefaultProfile</span></span>
<span data-ttu-id="d84f2-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d84f2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d84f2-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="d84f2-112">-Name</span></span>
<span data-ttu-id="d84f2-113">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="d84f2-113">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d84f2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d84f2-114">-ResourceGroupName</span></span>
<span data-ttu-id="d84f2-115">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="d84f2-115">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d84f2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84f2-116">CommonParameters</span></span>
<span data-ttu-id="d84f2-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d84f2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84f2-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d84f2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84f2-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d84f2-119">INPUTS</span></span>

### <span data-ttu-id="d84f2-120">System. String</span><span class="sxs-lookup"><span data-stu-id="d84f2-120">System.String</span></span>

## <span data-ttu-id="d84f2-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d84f2-121">OUTPUTS</span></span>

### <span data-ttu-id="d84f2-122">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d84f2-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="d84f2-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d84f2-123">NOTES</span></span>

## <span data-ttu-id="d84f2-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d84f2-124">RELATED LINKS</span></span>