---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8f0fc8caba03251ede507fc383ef99c10a06eeb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760669"
---
# <span data-ttu-id="d22dc-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="d22dc-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="d22dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d22dc-102">SYNOPSIS</span></span>
<span data-ttu-id="d22dc-103">Desteklenen sunucu değişkenlerini ve kullanılabilir istek ve yanıt üst bilgilerini alın.</span><span class="sxs-lookup"><span data-stu-id="d22dc-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="d22dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d22dc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="d22dc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d22dc-105">DESCRIPTION</span></span>
<span data-ttu-id="d22dc-106">**Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet 'i, desteklenen sunucu değişkenlerini ve kullanılabilir istek ve yanıt üstbilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="d22dc-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="d22dc-107">Parametreler, değişkenler veya üstbilgiler listelerini almak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d22dc-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="d22dc-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d22dc-108">EXAMPLES</span></span>

### <span data-ttu-id="d22dc-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d22dc-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="d22dc-110">Bu komut, kullanılabilen tüm sunucu değişkenlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d22dc-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="d22dc-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d22dc-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="d22dc-112">Bu komut, kullanılabilen tüm istek üstbilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d22dc-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="d22dc-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="d22dc-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="d22dc-114">Bu komut, kullanılabilir tüm yanıt üstbilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d22dc-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="d22dc-115">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="d22dc-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="d22dc-116">Bu komut kullanılabilir tüm sunucu değişkenlerini, istek ve yanıt üstbilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d22dc-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="d22dc-117">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="d22dc-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="d22dc-118">Bu komut kullanılabilir tüm sunucu değişkenlerini, istek ve yanıt üstbilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d22dc-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="d22dc-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d22dc-119">PARAMETERS</span></span>

### <span data-ttu-id="d22dc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22dc-120">-DefaultProfile</span></span>
<span data-ttu-id="d22dc-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d22dc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d22dc-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="d22dc-122">-RequestHeader</span></span>
<span data-ttu-id="d22dc-123">Uygulama ağ geçidi kullanılabilir istek üst bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d22dc-123">Application Gateway available request headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22dc-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="d22dc-124">-ResponseHeader</span></span>
<span data-ttu-id="d22dc-125">Uygulama ağ geçidi kullanılabilir yanıt üst bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d22dc-125">Application Gateway available response headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22dc-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="d22dc-126">-ServerVariable</span></span>
<span data-ttu-id="d22dc-127">Uygulama ağ geçidi kullanılabilir sunucu değişkenleri.</span><span class="sxs-lookup"><span data-stu-id="d22dc-127">Application Gateway available server variables.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22dc-128">CommonParameters</span></span>
<span data-ttu-id="d22dc-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d22dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22dc-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d22dc-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22dc-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d22dc-131">INPUTS</span></span>

### <span data-ttu-id="d22dc-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d22dc-132">None</span></span>

## <span data-ttu-id="d22dc-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d22dc-133">OUTPUTS</span></span>

### <span data-ttu-id="d22dc-134">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="d22dc-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="d22dc-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d22dc-135">NOTES</span></span>
<span data-ttu-id="d22dc-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** , **Get-azapplicationgatewayavailableservervariableveheader** cmdlet 'inin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="d22dc-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="d22dc-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d22dc-137">RELATED LINKS</span></span>
