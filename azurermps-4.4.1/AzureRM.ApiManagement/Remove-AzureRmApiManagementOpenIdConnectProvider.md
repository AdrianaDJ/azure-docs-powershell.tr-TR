---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 686b988ef5bf62e5eed7e4f8fae94f6b29b1b4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588312"
---
# <span data-ttu-id="86adf-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="86adf-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="86adf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86adf-102">SYNOPSIS</span></span>
<span data-ttu-id="86adf-103">OpenID Connect sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="86adf-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86adf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="86adf-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86adf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="86adf-105">DESCRIPTION</span></span>
<span data-ttu-id="86adf-106">**Remove-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı, Azure API Yönetimi Için OpenID Connect sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="86adf-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="86adf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="86adf-107">EXAMPLES</span></span>

### <span data-ttu-id="86adf-108">Örnek 1: sağlayıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="86adf-108">Example 1: Remove a provider</span></span>
```
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="86adf-109">Bu komut, KIMLIĞI OICProvicer01 olan sağlayıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="86adf-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="86adf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="86adf-110">PARAMETERS</span></span>

### <span data-ttu-id="86adf-111">-Context</span><span class="sxs-lookup"><span data-stu-id="86adf-111">-Context</span></span>
<span data-ttu-id="86adf-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="86adf-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="86adf-113">-Openıdconnectproviderıd</span><span class="sxs-lookup"><span data-stu-id="86adf-113">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="86adf-114">Bu cmdlet 'in kaldırdığı sağlayıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="86adf-114">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="86adf-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="86adf-115">-PassThru</span></span>
<span data-ttu-id="86adf-116">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="86adf-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="86adf-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="86adf-117">-Confirm</span></span>
<span data-ttu-id="86adf-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="86adf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86adf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86adf-119">-WhatIf</span></span>
<span data-ttu-id="86adf-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="86adf-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86adf-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="86adf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86adf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86adf-122">-DefaultProfile</span></span>
<span data-ttu-id="86adf-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="86adf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86adf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86adf-124">CommonParameters</span></span>
<span data-ttu-id="86adf-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="86adf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86adf-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86adf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86adf-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="86adf-127">INPUTS</span></span>

## <span data-ttu-id="86adf-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="86adf-128">OUTPUTS</span></span>

### <span data-ttu-id="86adf-129">Boole</span><span class="sxs-lookup"><span data-stu-id="86adf-129">Boolean</span></span>

## <span data-ttu-id="86adf-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="86adf-130">NOTES</span></span>

## <span data-ttu-id="86adf-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="86adf-131">RELATED LINKS</span></span>

[<span data-ttu-id="86adf-132">Get-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="86adf-132">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="86adf-133">Yeni-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="86adf-133">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="86adf-134">Set-Azurermapımanagementopenıdconnectprovider</span><span class="sxs-lookup"><span data-stu-id="86adf-134">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


