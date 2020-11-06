---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6b4ccac87f963f9948c67d3162f1677b9860583b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573029"
---
# <span data-ttu-id="a0a7e-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a0a7e-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="a0a7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a7e-103">OpenID Connect sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0a7e-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0a7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0a7e-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0a7e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0a7e-105">DESCRIPTION</span></span>
<span data-ttu-id="a0a7e-106">**Remove-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı, Azure API Yönetimi Için OpenID Connect sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0a7e-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="a0a7e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0a7e-107">EXAMPLES</span></span>

### <span data-ttu-id="a0a7e-108">Örnek 1: sağlayıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="a0a7e-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="a0a7e-109">Bu komut, KIMLIĞI OICProvicer01 olan sağlayıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0a7e-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="a0a7e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0a7e-110">PARAMETERS</span></span>

### <span data-ttu-id="a0a7e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a0a7e-111">-Context</span></span>
<span data-ttu-id="a0a7e-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0a7e-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a0a7e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a7e-113">-DefaultProfile</span></span>
<span data-ttu-id="a0a7e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0a7e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0a7e-115">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="a0a7e-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="a0a7e-116">Bu cmdlet 'in kaldırdığı sağlayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0a7e-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a0a7e-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a0a7e-117">-PassThru</span></span>
<span data-ttu-id="a0a7e-118">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="a0a7e-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="a0a7e-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0a7e-119">-Confirm</span></span>
<span data-ttu-id="a0a7e-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0a7e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a7e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0a7e-121">-WhatIf</span></span>
<span data-ttu-id="a0a7e-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0a7e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0a7e-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0a7e-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a7e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a7e-124">CommonParameters</span></span>
<span data-ttu-id="a0a7e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0a7e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a7e-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0a7e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a7e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0a7e-127">INPUTS</span></span>

### <span data-ttu-id="a0a7e-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="a0a7e-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a0a7e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a0a7e-129">System.String</span></span>

### <span data-ttu-id="a0a7e-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a0a7e-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a0a7e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0a7e-131">OUTPUTS</span></span>

### <span data-ttu-id="a0a7e-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0a7e-132">System.Boolean</span></span>

## <span data-ttu-id="a0a7e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0a7e-133">NOTES</span></span>

## <span data-ttu-id="a0a7e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0a7e-134">RELATED LINKS</span></span>

[<span data-ttu-id="a0a7e-135">Get-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="a0a7e-135">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a0a7e-136">Yeni-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="a0a7e-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a0a7e-137">Set-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="a0a7e-137">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


