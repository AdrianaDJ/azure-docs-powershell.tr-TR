---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: 2eba88e94cfed3c253a5b5febc20a7585ab096d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586841"
---
# <span data-ttu-id="8381e-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="8381e-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="8381e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8381e-102">SYNOPSIS</span></span>
<span data-ttu-id="8381e-103">Bir gruptan bir ürünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8381e-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8381e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8381e-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8381e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8381e-105">DESCRIPTION</span></span>
<span data-ttu-id="8381e-106">**Remove-Azurermapsananagementproductfromgroup** cmdlet 'i var olan bir gruptan bir ürünü çıkarır.</span><span class="sxs-lookup"><span data-stu-id="8381e-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="8381e-107">Başka bir deyişle, bu cmdlet bir üründen grup atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8381e-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="8381e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8381e-108">EXAMPLES</span></span>

### <span data-ttu-id="8381e-109">Örnek 1: gruptan ürün kaldırma</span><span class="sxs-lookup"><span data-stu-id="8381e-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="8381e-110">Bu komut, mevcut bir gruptan bir ürünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8381e-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="8381e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8381e-111">PARAMETERS</span></span>

### <span data-ttu-id="8381e-112">-Context</span><span class="sxs-lookup"><span data-stu-id="8381e-112">-Context</span></span>
<span data-ttu-id="8381e-113">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8381e-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="8381e-114">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8381e-114">This parameter is required.</span></span>

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

### <span data-ttu-id="8381e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8381e-115">-DefaultProfile</span></span>
<span data-ttu-id="8381e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8381e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="8381e-117">-GroupID</span><span class="sxs-lookup"><span data-stu-id="8381e-117">-GroupId</span></span>
<span data-ttu-id="8381e-118">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8381e-118">Specifies the group ID.</span></span>
<span data-ttu-id="8381e-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8381e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="8381e-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8381e-120">-PassThru</span></span>
<span data-ttu-id="8381e-121">Bu cmdlet 'in $True değeri (başarılı olursa) veya $False olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8381e-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="8381e-122">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="8381e-122">-ProductId</span></span>
<span data-ttu-id="8381e-123">Ürün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8381e-123">Specifies the product ID.</span></span>
<span data-ttu-id="8381e-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8381e-124">This parameter is required.</span></span>

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

### <span data-ttu-id="8381e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8381e-125">CommonParameters</span></span>
<span data-ttu-id="8381e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8381e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8381e-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8381e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8381e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8381e-128">INPUTS</span></span>

### <span data-ttu-id="8381e-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8381e-129">None</span></span>
<span data-ttu-id="8381e-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8381e-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8381e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8381e-131">OUTPUTS</span></span>

### <span data-ttu-id="8381e-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8381e-132">System.Boolean</span></span>

## <span data-ttu-id="8381e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8381e-133">NOTES</span></span>

## <span data-ttu-id="8381e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8381e-134">RELATED LINKS</span></span>

[<span data-ttu-id="8381e-135">Add-Azurermapımanagementproducttogroup</span><span class="sxs-lookup"><span data-stu-id="8381e-135">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


