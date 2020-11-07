---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 5258b041f2858ce766f5b6e932412986545ccf13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917776"
---
# <span data-ttu-id="453f0-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="453f0-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="453f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="453f0-102">SYNOPSIS</span></span>
<span data-ttu-id="453f0-103">Var olan kimlik sağlayıcı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="453f0-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="453f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="453f0-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="453f0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="453f0-105">DESCRIPTION</span></span>
<span data-ttu-id="453f0-106">Var olan kimlik sağlayıcı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="453f0-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="453f0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="453f0-107">EXAMPLES</span></span>

### <span data-ttu-id="453f0-108">Facebook kimlik sağlayıcısı ayarlarını, Apımanayönetimi hizmetinden kaldırır</span><span class="sxs-lookup"><span data-stu-id="453f0-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="453f0-109">Facebook Identity Provider yapılandırması ile ilgili yapılandırmayı siler.</span><span class="sxs-lookup"><span data-stu-id="453f0-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="453f0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="453f0-110">PARAMETERS</span></span>

### <span data-ttu-id="453f0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="453f0-111">-Context</span></span>
<span data-ttu-id="453f0-112">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="453f0-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="453f0-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="453f0-113">This parameter is required.</span></span>

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

### <span data-ttu-id="453f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="453f0-114">-DefaultProfile</span></span>
<span data-ttu-id="453f0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="453f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="453f0-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="453f0-116">-PassThru</span></span>
<span data-ttu-id="453f0-117">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="453f0-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="453f0-118">-Tür</span><span class="sxs-lookup"><span data-stu-id="453f0-118">-Type</span></span>
<span data-ttu-id="453f0-119">Var olan bir kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="453f0-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="453f0-120">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="453f0-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="453f0-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="453f0-121">-Confirm</span></span>
<span data-ttu-id="453f0-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="453f0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="453f0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="453f0-123">-WhatIf</span></span>
<span data-ttu-id="453f0-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="453f0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="453f0-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="453f0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="453f0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="453f0-126">CommonParameters</span></span>
<span data-ttu-id="453f0-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="453f0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="453f0-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="453f0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="453f0-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="453f0-129">INPUTS</span></span>

### <span data-ttu-id="453f0-130">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="453f0-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="453f0-131">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovidertype</span><span class="sxs-lookup"><span data-stu-id="453f0-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="453f0-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="453f0-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="453f0-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="453f0-133">OUTPUTS</span></span>

### <span data-ttu-id="453f0-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="453f0-134">System.Boolean</span></span>

## <span data-ttu-id="453f0-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="453f0-135">NOTES</span></span>

## <span data-ttu-id="453f0-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="453f0-136">RELATED LINKS</span></span>

[<span data-ttu-id="453f0-137">Yeni-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="453f0-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="453f0-138">Get-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="453f0-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="453f0-139">Set-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="453f0-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

