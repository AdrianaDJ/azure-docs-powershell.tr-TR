---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 957a2fbecc588f9b04400571e587c6ba56e16df5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587035"
---
# <span data-ttu-id="9eed6-101">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="9eed6-101">Remove-AzureRmApiManagementApiFromProduct</span></span>

## <span data-ttu-id="9eed6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eed6-102">SYNOPSIS</span></span>
<span data-ttu-id="9eed6-103">Bir üründen API 'YI kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9eed6-103">Removes an API from a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9eed6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9eed6-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eed6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9eed6-105">DESCRIPTION</span></span>
<span data-ttu-id="9eed6-106">**Remove-Azurermapımanagementapifromproduct** cmdlet 'i bir üründen Azure API yönetim API 'sini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9eed6-106">The **Remove-AzureRmApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="9eed6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9eed6-107">EXAMPLES</span></span>

### <span data-ttu-id="9eed6-108">Örnek 1: bir üründen API 'YI kaldırma</span><span class="sxs-lookup"><span data-stu-id="9eed6-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="9eed6-109">Bu işlem, belirtilen API 'YI üründen kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9eed6-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="9eed6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9eed6-110">PARAMETERS</span></span>

### <span data-ttu-id="9eed6-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="9eed6-111">-ApiId</span></span>
<span data-ttu-id="9eed6-112">Üründen kaldırılacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9eed6-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="9eed6-113">-Context</span><span class="sxs-lookup"><span data-stu-id="9eed6-113">-Context</span></span>
<span data-ttu-id="9eed6-114">**Psapsananabir Gementcontext** belirtir.</span><span class="sxs-lookup"><span data-stu-id="9eed6-114">Specifies a **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eed6-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9eed6-115">-PassThru</span></span>
<span data-ttu-id="9eed6-116">Bu cmdlet 'in başarılı olduğu bir $True değerini (veya $False) döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9eed6-116">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eed6-117">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="9eed6-117">-ProductId</span></span>
<span data-ttu-id="9eed6-118">API 'nin kaldırılacağı ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9eed6-118">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="9eed6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eed6-119">-DefaultProfile</span></span>
<span data-ttu-id="9eed6-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9eed6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eed6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eed6-121">CommonParameters</span></span>
<span data-ttu-id="9eed6-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9eed6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eed6-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eed6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eed6-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9eed6-124">INPUTS</span></span>

## <span data-ttu-id="9eed6-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9eed6-125">OUTPUTS</span></span>

### <span data-ttu-id="9eed6-126">bool</span><span class="sxs-lookup"><span data-stu-id="9eed6-126">bool</span></span>

## <span data-ttu-id="9eed6-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9eed6-127">NOTES</span></span>

## <span data-ttu-id="9eed6-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9eed6-128">RELATED LINKS</span></span>

[<span data-ttu-id="9eed6-129">Add-Azurermapımanagementapitoproduct</span><span class="sxs-lookup"><span data-stu-id="9eed6-129">Add-AzureRmApiManagementApiToProduct</span></span>](./Add-AzureRmApiManagementApiToProduct.md)


