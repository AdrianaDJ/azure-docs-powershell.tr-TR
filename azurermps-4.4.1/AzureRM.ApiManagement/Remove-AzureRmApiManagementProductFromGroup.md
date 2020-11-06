---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: a6ef7e141863b6dfd98185df0f8e3cfbd85ae40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587026"
---
# <span data-ttu-id="11e85-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="11e85-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="11e85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11e85-102">SYNOPSIS</span></span>
<span data-ttu-id="11e85-103">Bir gruptan bir ürünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="11e85-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11e85-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11e85-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11e85-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="11e85-105">DESCRIPTION</span></span>
<span data-ttu-id="11e85-106">**Remove-Azurermapsananagementproductfromgroup** cmdlet 'i var olan bir gruptan bir ürünü çıkarır.</span><span class="sxs-lookup"><span data-stu-id="11e85-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="11e85-107">Başka bir deyişle, bu cmdlet bir üründen grup atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="11e85-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="11e85-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11e85-108">EXAMPLES</span></span>

### <span data-ttu-id="11e85-109">Örnek 1: gruptan ürün kaldırma</span><span class="sxs-lookup"><span data-stu-id="11e85-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="11e85-110">Bu komut, mevcut bir gruptan bir ürünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="11e85-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="11e85-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11e85-111">PARAMETERS</span></span>

### <span data-ttu-id="11e85-112">-Context</span><span class="sxs-lookup"><span data-stu-id="11e85-112">-Context</span></span>
<span data-ttu-id="11e85-113">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="11e85-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="11e85-114">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="11e85-114">This parameter is required.</span></span>

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

### <span data-ttu-id="11e85-115">-GroupID</span><span class="sxs-lookup"><span data-stu-id="11e85-115">-GroupId</span></span>
<span data-ttu-id="11e85-116">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="11e85-116">Specifies the group ID.</span></span>
<span data-ttu-id="11e85-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="11e85-117">This parameter is required.</span></span>

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

### <span data-ttu-id="11e85-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="11e85-118">-PassThru</span></span>
<span data-ttu-id="11e85-119">Bu cmdlet 'in $True değeri (başarılı olursa) veya $False olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="11e85-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="11e85-120">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="11e85-120">-ProductId</span></span>
<span data-ttu-id="11e85-121">Ürün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="11e85-121">Specifies the product ID.</span></span>
<span data-ttu-id="11e85-122">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="11e85-122">This parameter is required.</span></span>

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

### <span data-ttu-id="11e85-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e85-123">-DefaultProfile</span></span>
<span data-ttu-id="11e85-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11e85-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11e85-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e85-125">CommonParameters</span></span>
<span data-ttu-id="11e85-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11e85-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e85-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11e85-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e85-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11e85-128">INPUTS</span></span>

## <span data-ttu-id="11e85-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11e85-129">OUTPUTS</span></span>

### <span data-ttu-id="11e85-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11e85-130">System.Boolean</span></span>

## <span data-ttu-id="11e85-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11e85-131">NOTES</span></span>

## <span data-ttu-id="11e85-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11e85-132">RELATED LINKS</span></span>

[<span data-ttu-id="11e85-133">Add-Azurermapımanagementproducttogroup</span><span class="sxs-lookup"><span data-stu-id="11e85-133">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


