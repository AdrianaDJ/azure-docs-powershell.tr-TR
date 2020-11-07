---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f148f65a6065040a28f936a5dec64f09ff4045eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753459"
---
# <span data-ttu-id="8782f-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8782f-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="8782f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8782f-102">SYNOPSIS</span></span>
<span data-ttu-id="8782f-103">OpenID Connect sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8782f-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="8782f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8782f-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8782f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8782f-105">DESCRIPTION</span></span>
<span data-ttu-id="8782f-106">**Remove-Azapsananagementopenıdconnectprovider** cmdlet 'ı Azure API Yönetimi Için OpenID Connect sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8782f-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="8782f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8782f-107">EXAMPLES</span></span>

### <span data-ttu-id="8782f-108">Örnek 1: sağlayıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="8782f-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="8782f-109">Bu komut, KIMLIĞI OICProvider01 olan sağlayıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8782f-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="8782f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8782f-110">PARAMETERS</span></span>

### <span data-ttu-id="8782f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8782f-111">-Context</span></span>
<span data-ttu-id="8782f-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8782f-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8782f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8782f-113">-DefaultProfile</span></span>
<span data-ttu-id="8782f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8782f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8782f-115">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="8782f-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="8782f-116">Bu cmdlet 'in kaldırdığı sağlayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8782f-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8782f-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8782f-117">-PassThru</span></span>
<span data-ttu-id="8782f-118">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="8782f-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="8782f-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="8782f-119">-Confirm</span></span>
<span data-ttu-id="8782f-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8782f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8782f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8782f-121">-WhatIf</span></span>
<span data-ttu-id="8782f-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8782f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8782f-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8782f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8782f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8782f-124">CommonParameters</span></span>
<span data-ttu-id="8782f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8782f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8782f-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8782f-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8782f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8782f-127">INPUTS</span></span>

### <span data-ttu-id="8782f-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="8782f-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8782f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8782f-129">System.String</span></span>

### <span data-ttu-id="8782f-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8782f-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8782f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8782f-131">OUTPUTS</span></span>

### <span data-ttu-id="8782f-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8782f-132">System.Boolean</span></span>

## <span data-ttu-id="8782f-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8782f-133">NOTES</span></span>

## <span data-ttu-id="8782f-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8782f-134">RELATED LINKS</span></span>

[<span data-ttu-id="8782f-135">Get-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="8782f-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="8782f-136">Yeni-Azapsananagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="8782f-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="8782f-137">Set-Azapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="8782f-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


