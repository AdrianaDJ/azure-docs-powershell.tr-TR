---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: 0d56528f2cbe827f4dfc5ba20e2a9f8c840256ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592821"
---
# <span data-ttu-id="a482c-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="a482c-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="a482c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a482c-102">SYNOPSIS</span></span>
<span data-ttu-id="a482c-103">Bir gruptan bir ürünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a482c-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a482c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a482c-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a482c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a482c-105">DESCRIPTION</span></span>
<span data-ttu-id="a482c-106">**Remove-Azurermapsananagementproductfromgroup** cmdlet 'i var olan bir gruptan bir ürünü çıkarır.</span><span class="sxs-lookup"><span data-stu-id="a482c-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="a482c-107">Başka bir deyişle, bu cmdlet bir üründen grup atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a482c-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="a482c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a482c-108">EXAMPLES</span></span>

### <span data-ttu-id="a482c-109">Örnek 1: gruptan ürün kaldırma</span><span class="sxs-lookup"><span data-stu-id="a482c-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="a482c-110">Bu komut, mevcut bir gruptan bir ürünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a482c-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="a482c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a482c-111">PARAMETERS</span></span>

### <span data-ttu-id="a482c-112">-Context</span><span class="sxs-lookup"><span data-stu-id="a482c-112">-Context</span></span>
<span data-ttu-id="a482c-113">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a482c-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="a482c-114">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a482c-114">This parameter is required.</span></span>

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

### <span data-ttu-id="a482c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a482c-115">-DefaultProfile</span></span>
<span data-ttu-id="a482c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a482c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a482c-117">-GroupID</span><span class="sxs-lookup"><span data-stu-id="a482c-117">-GroupId</span></span>
<span data-ttu-id="a482c-118">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a482c-118">Specifies the group ID.</span></span>
<span data-ttu-id="a482c-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a482c-119">This parameter is required.</span></span>

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

### <span data-ttu-id="a482c-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a482c-120">-PassThru</span></span>
<span data-ttu-id="a482c-121">Bu cmdlet 'in $True değeri (başarılı olursa) veya $False olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a482c-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="a482c-122">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="a482c-122">-ProductId</span></span>
<span data-ttu-id="a482c-123">Ürün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a482c-123">Specifies the product ID.</span></span>
<span data-ttu-id="a482c-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a482c-124">This parameter is required.</span></span>

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

### <span data-ttu-id="a482c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a482c-125">CommonParameters</span></span>
<span data-ttu-id="a482c-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a482c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a482c-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a482c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a482c-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a482c-128">INPUTS</span></span>

### <span data-ttu-id="a482c-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="a482c-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a482c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a482c-130">System.String</span></span>

### <span data-ttu-id="a482c-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a482c-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a482c-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a482c-132">OUTPUTS</span></span>

### <span data-ttu-id="a482c-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a482c-133">System.Boolean</span></span>

## <span data-ttu-id="a482c-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a482c-134">NOTES</span></span>

## <span data-ttu-id="a482c-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a482c-135">RELATED LINKS</span></span>

[<span data-ttu-id="a482c-136">Add-Azurermapımanagementproducttogroup</span><span class="sxs-lookup"><span data-stu-id="a482c-136">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


