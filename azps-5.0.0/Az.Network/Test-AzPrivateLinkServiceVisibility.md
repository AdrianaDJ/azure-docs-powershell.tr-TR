---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: f443928a8a616e8b8c6c13e5ae941aff607638ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325168"
---
# <span data-ttu-id="d68a1-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="d68a1-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="d68a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d68a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d68a1-103">**Test-Azprivatelinkservici bility** , özel bir bağlantı hizmetinin geçerli kullanımda olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="d68a1-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="d68a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d68a1-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d68a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d68a1-105">DESCRIPTION</span></span>
<span data-ttu-id="d68a1-106">Geçerli kullanımda özel bir bağlantı hizmeti olup olmadığını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="d68a1-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="d68a1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d68a1-107">EXAMPLES</span></span>

### <span data-ttu-id="d68a1-108">Örnek 1: contoso.cloudapp.azure.com 'in kullanılabilir olup olmadığını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="d68a1-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="d68a1-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d68a1-109">PARAMETERS</span></span>

### <span data-ttu-id="d68a1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68a1-110">-DefaultProfile</span></span>
<span data-ttu-id="d68a1-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d68a1-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d68a1-112">-Konum</span><span class="sxs-lookup"><span data-stu-id="d68a1-112">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d68a1-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="d68a1-113">-PrivateLinkServiceAlias</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68a1-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d68a1-114">-ResourceGroupName</span></span>
<span data-ttu-id="d68a1-115">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d68a1-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d68a1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68a1-116">CommonParameters</span></span>
<span data-ttu-id="d68a1-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d68a1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68a1-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d68a1-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68a1-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d68a1-119">INPUTS</span></span>

### <span data-ttu-id="d68a1-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d68a1-120">None</span></span>

## <span data-ttu-id="d68a1-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d68a1-121">OUTPUTS</span></span>

### <span data-ttu-id="d68a1-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d68a1-122">System.Boolean</span></span>

## <span data-ttu-id="d68a1-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d68a1-123">NOTES</span></span>

## <span data-ttu-id="d68a1-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d68a1-124">RELATED LINKS</span></span>
