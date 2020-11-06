---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 03f56a17d038407b3a33c09188c9a29b6f4caf09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588321"
---
# <span data-ttu-id="90555-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="90555-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="90555-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90555-102">SYNOPSIS</span></span>
<span data-ttu-id="90555-103">Arka uç 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="90555-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90555-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90555-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90555-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="90555-105">DESCRIPTION</span></span>
<span data-ttu-id="90555-106">Tanımlayıcının belirttiği arka uç API yönetiminden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="90555-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="90555-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90555-107">EXAMPLES</span></span>

### <span data-ttu-id="90555-108">Örnek 1: arka uç 123</span><span class="sxs-lookup"><span data-stu-id="90555-108">Example 1: Remove the Backend 123</span></span>
```
Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="90555-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90555-109">PARAMETERS</span></span>

### <span data-ttu-id="90555-110">-Backenmuydunuz</span><span class="sxs-lookup"><span data-stu-id="90555-110">-BackendId</span></span>
<span data-ttu-id="90555-111">Var olan arka ucun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="90555-111">Identifier of existing backend.</span></span>
<span data-ttu-id="90555-112">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="90555-112">This parameter is required.</span></span>

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

### <span data-ttu-id="90555-113">-Context</span><span class="sxs-lookup"><span data-stu-id="90555-113">-Context</span></span>
<span data-ttu-id="90555-114">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="90555-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="90555-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="90555-115">This parameter is required.</span></span>

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

### <span data-ttu-id="90555-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="90555-116">-PassThru</span></span>
<span data-ttu-id="90555-117">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="90555-117">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="90555-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="90555-118">This parameter is optional.</span></span>
<span data-ttu-id="90555-119">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="90555-119">Default value is false.</span></span>

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

### <span data-ttu-id="90555-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="90555-120">-Confirm</span></span>
<span data-ttu-id="90555-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90555-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90555-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90555-122">-WhatIf</span></span>
<span data-ttu-id="90555-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90555-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90555-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90555-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90555-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90555-125">-DefaultProfile</span></span>
<span data-ttu-id="90555-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90555-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90555-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90555-127">CommonParameters</span></span>
<span data-ttu-id="90555-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90555-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90555-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90555-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90555-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90555-130">INPUTS</span></span>

## <span data-ttu-id="90555-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90555-131">OUTPUTS</span></span>

### <span data-ttu-id="90555-132">bool</span><span class="sxs-lookup"><span data-stu-id="90555-132">bool</span></span>

## <span data-ttu-id="90555-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90555-133">NOTES</span></span>

## <span data-ttu-id="90555-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90555-134">RELATED LINKS</span></span>

[<span data-ttu-id="90555-135">Get-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="90555-135">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="90555-136">Yeni-Azurermapsananaarka uç</span><span class="sxs-lookup"><span data-stu-id="90555-136">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="90555-137">Yeni-Azurermapımanagementbackendcredential</span><span class="sxs-lookup"><span data-stu-id="90555-137">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="90555-138">Yeni-Azurermapımanagementbackendproxy</span><span class="sxs-lookup"><span data-stu-id="90555-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="90555-139">Set-Azurermapımanaarka uç</span><span class="sxs-lookup"><span data-stu-id="90555-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
