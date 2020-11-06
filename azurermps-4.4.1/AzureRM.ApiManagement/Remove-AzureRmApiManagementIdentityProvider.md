---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: ecbb2b6671f1482f31cb7b3f0b07d4e9be4bbb3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588317"
---
# <span data-ttu-id="63501-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="63501-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="63501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63501-102">SYNOPSIS</span></span>
<span data-ttu-id="63501-103">Var olan kimlik sağlayıcı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="63501-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63501-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63501-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63501-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="63501-105">DESCRIPTION</span></span>
<span data-ttu-id="63501-106">Var olan kimlik sağlayıcı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="63501-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="63501-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63501-107">EXAMPLES</span></span>

### <span data-ttu-id="63501-108">Facebook kimlik sağlayıcısı ayarlarını, Apımanayönetimi hizmetinden kaldırır</span><span class="sxs-lookup"><span data-stu-id="63501-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="63501-109">Facebook Identity Provider yapılandırması ile ilgili yapılandırmayı siler.</span><span class="sxs-lookup"><span data-stu-id="63501-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="63501-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63501-110">PARAMETERS</span></span>

### <span data-ttu-id="63501-111">-Context</span><span class="sxs-lookup"><span data-stu-id="63501-111">-Context</span></span>
<span data-ttu-id="63501-112">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="63501-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="63501-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="63501-113">This parameter is required.</span></span>

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

### <span data-ttu-id="63501-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="63501-114">-PassThru</span></span>
<span data-ttu-id="63501-115">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="63501-115">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


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

### <span data-ttu-id="63501-116">-Tür</span><span class="sxs-lookup"><span data-stu-id="63501-116">-Type</span></span>
<span data-ttu-id="63501-117">Var olan bir kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="63501-117">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="63501-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="63501-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63501-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="63501-119">-Confirm</span></span>
<span data-ttu-id="63501-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="63501-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63501-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63501-121">-WhatIf</span></span>
<span data-ttu-id="63501-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="63501-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63501-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="63501-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63501-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63501-124">-DefaultProfile</span></span>
<span data-ttu-id="63501-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63501-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63501-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63501-126">CommonParameters</span></span>
<span data-ttu-id="63501-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63501-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63501-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63501-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63501-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63501-129">INPUTS</span></span>

## <span data-ttu-id="63501-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63501-130">OUTPUTS</span></span>

### <span data-ttu-id="63501-131">bool</span><span class="sxs-lookup"><span data-stu-id="63501-131">bool</span></span>

## <span data-ttu-id="63501-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63501-132">NOTES</span></span>

## <span data-ttu-id="63501-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63501-133">RELATED LINKS</span></span>

[<span data-ttu-id="63501-134">Yeni-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="63501-134">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="63501-135">Get-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="63501-135">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="63501-136">Set-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="63501-136">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

