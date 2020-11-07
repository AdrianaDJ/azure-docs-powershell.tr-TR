---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: 4bcda06e1c00e338feb80584fb6e2b51a63b051d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764740"
---
# <span data-ttu-id="c20a3-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c20a3-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="c20a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c20a3-102">SYNOPSIS</span></span>
<span data-ttu-id="c20a3-103">Bir API 'YI kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c20a3-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c20a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c20a3-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c20a3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c20a3-105">DESCRIPTION</span></span>
<span data-ttu-id="c20a3-106">**Remove-Azurermapsananagementapı** cmdlet 'i var olan bir API 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c20a3-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="c20a3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c20a3-107">EXAMPLES</span></span>

### <span data-ttu-id="c20a3-108">Örnek 1: API 'YI kaldırma</span><span class="sxs-lookup"><span data-stu-id="c20a3-108">Example 1: Remove an API</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="c20a3-109">Bu komut belirtilen KIMLIKLE API 'YI kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c20a3-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="c20a3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c20a3-110">PARAMETERS</span></span>

### <span data-ttu-id="c20a3-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="c20a3-111">-ApiId</span></span>
<span data-ttu-id="c20a3-112">API kaldırma KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c20a3-112">Specifies the ID of the API remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c20a3-113">-Context</span><span class="sxs-lookup"><span data-stu-id="c20a3-113">-Context</span></span>
<span data-ttu-id="c20a3-114">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c20a3-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c20a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c20a3-115">-DefaultProfile</span></span>
<span data-ttu-id="c20a3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c20a3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="c20a3-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c20a3-117">-PassThru</span></span>
<span data-ttu-id="c20a3-118">geçiş</span><span class="sxs-lookup"><span data-stu-id="c20a3-118">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c20a3-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="c20a3-119">-Confirm</span></span>
<span data-ttu-id="c20a3-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c20a3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20a3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c20a3-121">-WhatIf</span></span>
<span data-ttu-id="c20a3-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c20a3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c20a3-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c20a3-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c20a3-124">CommonParameters</span></span>
<span data-ttu-id="c20a3-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c20a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c20a3-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c20a3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c20a3-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c20a3-127">INPUTS</span></span>

### <span data-ttu-id="c20a3-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c20a3-128">None</span></span>
<span data-ttu-id="c20a3-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c20a3-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c20a3-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c20a3-130">OUTPUTS</span></span>

### <span data-ttu-id="c20a3-131">Boole</span><span class="sxs-lookup"><span data-stu-id="c20a3-131">Boolean</span></span>

## <span data-ttu-id="c20a3-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c20a3-132">NOTES</span></span>

## <span data-ttu-id="c20a3-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c20a3-133">RELATED LINKS</span></span>

[<span data-ttu-id="c20a3-134">Dışarı aktarma-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="c20a3-134">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="c20a3-135">Get-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="c20a3-135">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="c20a3-136">Import-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="c20a3-136">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="c20a3-137">Yeni-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="c20a3-137">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="c20a3-138">Set-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="c20a3-138">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


