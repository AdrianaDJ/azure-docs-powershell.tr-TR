---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: c9133c7a2924b4151afd01f257fe6b54a9eeb00d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594515"
---
# <span data-ttu-id="145ad-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="145ad-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="145ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="145ad-102">SYNOPSIS</span></span>
<span data-ttu-id="145ad-103">Yetkilendirme sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="145ad-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="145ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="145ad-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="145ad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="145ad-105">DESCRIPTION</span></span>
<span data-ttu-id="145ad-106">**Remove-Azurermapsananagementauthorizationserver** cmdlet 'ı BIR Azure API yönetim yetkilendirme sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="145ad-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="145ad-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="145ad-107">EXAMPLES</span></span>

## <span data-ttu-id="145ad-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="145ad-108">PARAMETERS</span></span>

### <span data-ttu-id="145ad-109">-Context</span><span class="sxs-lookup"><span data-stu-id="145ad-109">-Context</span></span>
<span data-ttu-id="145ad-110">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="145ad-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="145ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="145ad-111">-DefaultProfile</span></span>
<span data-ttu-id="145ad-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="145ad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="145ad-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="145ad-113">-PassThru</span></span>
<span data-ttu-id="145ad-114">geçiş</span><span class="sxs-lookup"><span data-stu-id="145ad-114">passthru</span></span>

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

### <span data-ttu-id="145ad-115">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="145ad-115">-ServerId</span></span>
<span data-ttu-id="145ad-116">Kaldırılacak yetkilendirme sunucusunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="145ad-116">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="145ad-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="145ad-117">-Confirm</span></span>
<span data-ttu-id="145ad-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="145ad-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="145ad-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="145ad-119">-WhatIf</span></span>
<span data-ttu-id="145ad-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="145ad-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="145ad-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="145ad-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="145ad-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="145ad-122">CommonParameters</span></span>
<span data-ttu-id="145ad-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="145ad-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="145ad-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="145ad-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="145ad-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="145ad-125">INPUTS</span></span>

### <span data-ttu-id="145ad-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="145ad-126">None</span></span>
<span data-ttu-id="145ad-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="145ad-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="145ad-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="145ad-128">OUTPUTS</span></span>

### <span data-ttu-id="145ad-129">Boole</span><span class="sxs-lookup"><span data-stu-id="145ad-129">Boolean</span></span>

## <span data-ttu-id="145ad-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="145ad-130">NOTES</span></span>

## <span data-ttu-id="145ad-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="145ad-131">RELATED LINKS</span></span>

[<span data-ttu-id="145ad-132">Get-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="145ad-132">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="145ad-133">Yeni-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="145ad-133">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="145ad-134">Set-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="145ad-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


