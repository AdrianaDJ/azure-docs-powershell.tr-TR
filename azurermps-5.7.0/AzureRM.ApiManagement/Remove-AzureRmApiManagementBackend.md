---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 347a05c5e197a93458a64c4079ce1fd430e631f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590544"
---
# <span data-ttu-id="d42a5-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d42a5-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="d42a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d42a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d42a5-103">Arka uç 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d42a5-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d42a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d42a5-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d42a5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d42a5-105">DESCRIPTION</span></span>
<span data-ttu-id="d42a5-106">Tanımlayıcının belirttiği arka uç API yönetiminden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d42a5-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="d42a5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d42a5-107">EXAMPLES</span></span>

### <span data-ttu-id="d42a5-108">Örnek 1: arka uç 123</span><span class="sxs-lookup"><span data-stu-id="d42a5-108">Example 1: Remove the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="d42a5-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d42a5-109">PARAMETERS</span></span>

### <span data-ttu-id="d42a5-110">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="d42a5-110">-BackendId</span></span>
<span data-ttu-id="d42a5-111">Var olan arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="d42a5-111">Identifier of existing backend.</span></span>
<span data-ttu-id="d42a5-112">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d42a5-112">This parameter is required.</span></span>

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

### <span data-ttu-id="d42a5-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d42a5-113">-Context</span></span>
<span data-ttu-id="d42a5-114">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="d42a5-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d42a5-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d42a5-115">This parameter is required.</span></span>

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

### <span data-ttu-id="d42a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d42a5-116">-DefaultProfile</span></span>
<span data-ttu-id="d42a5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d42a5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d42a5-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d42a5-118">-PassThru</span></span>
<span data-ttu-id="d42a5-119">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="d42a5-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d42a5-120">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d42a5-120">This parameter is optional.</span></span>
<span data-ttu-id="d42a5-121">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="d42a5-121">Default value is false.</span></span>

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

### <span data-ttu-id="d42a5-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="d42a5-122">-Confirm</span></span>
<span data-ttu-id="d42a5-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d42a5-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42a5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d42a5-124">-WhatIf</span></span>
<span data-ttu-id="d42a5-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d42a5-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d42a5-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d42a5-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42a5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d42a5-127">CommonParameters</span></span>
<span data-ttu-id="d42a5-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d42a5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d42a5-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d42a5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d42a5-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d42a5-130">INPUTS</span></span>

### <span data-ttu-id="d42a5-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d42a5-131">None</span></span>
<span data-ttu-id="d42a5-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d42a5-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d42a5-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d42a5-133">OUTPUTS</span></span>

### <span data-ttu-id="d42a5-134">bool</span><span class="sxs-lookup"><span data-stu-id="d42a5-134">bool</span></span>

## <span data-ttu-id="d42a5-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d42a5-135">NOTES</span></span>

## <span data-ttu-id="d42a5-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d42a5-136">RELATED LINKS</span></span>

[<span data-ttu-id="d42a5-137">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="d42a5-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="d42a5-138">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="d42a5-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d42a5-139">Yeni-Azurermapımanagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="d42a5-139">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="d42a5-140">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="d42a5-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="d42a5-141">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="d42a5-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
