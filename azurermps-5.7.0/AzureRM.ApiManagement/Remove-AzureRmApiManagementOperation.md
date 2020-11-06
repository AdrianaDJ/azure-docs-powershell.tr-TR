---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: ef3db99522c07b593493e30bd3778f1774af1a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593766"
---
# <span data-ttu-id="52399-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="52399-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="52399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52399-102">SYNOPSIS</span></span>
<span data-ttu-id="52399-103">Var olan bir işlemi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="52399-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52399-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52399-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52399-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="52399-105">DESCRIPTION</span></span>
<span data-ttu-id="52399-106">**Remove-Azurermapsananagementoperation** cmdlet 'i var olan bir işlemi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="52399-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="52399-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52399-107">EXAMPLES</span></span>

### <span data-ttu-id="52399-108">Örnek 1: var olan bir API Işlemini kaldırma</span><span class="sxs-lookup"><span data-stu-id="52399-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="52399-109">Bu komut, var olan bir API Işlemini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="52399-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="52399-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52399-110">PARAMETERS</span></span>

### <span data-ttu-id="52399-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="52399-111">-ApiId</span></span>
<span data-ttu-id="52399-112">API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52399-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="52399-113">-Context</span><span class="sxs-lookup"><span data-stu-id="52399-113">-Context</span></span>
<span data-ttu-id="52399-114">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52399-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="52399-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52399-115">-DefaultProfile</span></span>
<span data-ttu-id="52399-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52399-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="52399-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="52399-117">-OperationId</span></span>
<span data-ttu-id="52399-118">API işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52399-118">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="52399-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="52399-119">-PassThru</span></span>
<span data-ttu-id="52399-120">Bu cmdlet 'in başarılı olduğu bir $True değerini veya $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52399-120">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="52399-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="52399-121">-Confirm</span></span>
<span data-ttu-id="52399-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="52399-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52399-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52399-123">-WhatIf</span></span>
<span data-ttu-id="52399-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52399-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52399-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="52399-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52399-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52399-126">CommonParameters</span></span>
<span data-ttu-id="52399-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52399-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52399-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52399-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52399-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52399-129">INPUTS</span></span>

### <span data-ttu-id="52399-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="52399-130">None</span></span>
<span data-ttu-id="52399-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="52399-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52399-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52399-132">OUTPUTS</span></span>

### <span data-ttu-id="52399-133">bool</span><span class="sxs-lookup"><span data-stu-id="52399-133">bool</span></span>

## <span data-ttu-id="52399-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52399-134">NOTES</span></span>

## <span data-ttu-id="52399-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52399-135">RELATED LINKS</span></span>

[<span data-ttu-id="52399-136">Get-Azurermapsananama</span><span class="sxs-lookup"><span data-stu-id="52399-136">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="52399-137">Yeni-Azurermapsananaks</span><span class="sxs-lookup"><span data-stu-id="52399-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="52399-138">Set-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="52399-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


