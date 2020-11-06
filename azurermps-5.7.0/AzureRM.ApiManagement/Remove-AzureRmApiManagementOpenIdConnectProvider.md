---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ee1ac7cda19f2b37ac1313d30075aa9c620bbd54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593763"
---
# <span data-ttu-id="8c7c5-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8c7c5-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="8c7c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c7c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7c5-103">OpenID Connect sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c7c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c7c5-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c7c5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c7c5-105">DESCRIPTION</span></span>
<span data-ttu-id="8c7c5-106">**Remove-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı, Azure API Yönetimi Için OpenID Connect sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="8c7c5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c7c5-107">EXAMPLES</span></span>

### <span data-ttu-id="8c7c5-108">Örnek 1: sağlayıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="8c7c5-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="8c7c5-109">Bu komut, KIMLIĞI OICProvicer01 olan sağlayıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="8c7c5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c7c5-110">PARAMETERS</span></span>

### <span data-ttu-id="8c7c5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8c7c5-111">-Context</span></span>
<span data-ttu-id="8c7c5-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8c7c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7c5-113">-DefaultProfile</span></span>
<span data-ttu-id="8c7c5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="8c7c5-115">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="8c7c5-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="8c7c5-116">Bu cmdlet 'in kaldırdığı sağlayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8c7c5-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8c7c5-117">-PassThru</span></span>
<span data-ttu-id="8c7c5-118">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="8c7c5-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="8c7c5-119">-Confirm</span></span>
<span data-ttu-id="8c7c5-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c7c5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c7c5-121">-WhatIf</span></span>
<span data-ttu-id="8c7c5-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c7c5-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c7c5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7c5-124">CommonParameters</span></span>
<span data-ttu-id="8c7c5-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7c5-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c7c5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7c5-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c7c5-127">INPUTS</span></span>

### <span data-ttu-id="8c7c5-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8c7c5-128">None</span></span>
<span data-ttu-id="8c7c5-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c7c5-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c7c5-130">OUTPUTS</span></span>

### <span data-ttu-id="8c7c5-131">Boole</span><span class="sxs-lookup"><span data-stu-id="8c7c5-131">Boolean</span></span>

## <span data-ttu-id="8c7c5-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c7c5-132">NOTES</span></span>

## <span data-ttu-id="8c7c5-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c7c5-133">RELATED LINKS</span></span>

[<span data-ttu-id="8c7c5-134">Get-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="8c7c5-134">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="8c7c5-135">Yeni-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="8c7c5-135">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="8c7c5-136">Set-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="8c7c5-136">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


