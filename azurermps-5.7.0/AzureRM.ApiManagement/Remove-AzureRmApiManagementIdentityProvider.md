---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 92e241703723d055d18083daae5fe424933f7c3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594150"
---
# <span data-ttu-id="4b1cc-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4b1cc-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="4b1cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b1cc-102">SYNOPSIS</span></span>
<span data-ttu-id="4b1cc-103">Var olan kimlik sağlayıcı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b1cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b1cc-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b1cc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b1cc-105">DESCRIPTION</span></span>
<span data-ttu-id="4b1cc-106">Var olan kimlik sağlayıcı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="4b1cc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b1cc-107">EXAMPLES</span></span>

### <span data-ttu-id="4b1cc-108">Facebook kimlik sağlayıcısı ayarlarını, Apımanayönetimi hizmetinden kaldırır</span><span class="sxs-lookup"><span data-stu-id="4b1cc-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="4b1cc-109">Facebook Identity Provider yapılandırması ile ilgili yapılandırmayı siler.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="4b1cc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b1cc-110">PARAMETERS</span></span>

### <span data-ttu-id="4b1cc-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4b1cc-111">-Context</span></span>
<span data-ttu-id="4b1cc-112">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4b1cc-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-113">This parameter is required.</span></span>

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

### <span data-ttu-id="4b1cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b1cc-114">-DefaultProfile</span></span>
<span data-ttu-id="4b1cc-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="4b1cc-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4b1cc-116">-PassThru</span></span>
<span data-ttu-id="4b1cc-117">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


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

### <span data-ttu-id="4b1cc-118">-Tür</span><span class="sxs-lookup"><span data-stu-id="4b1cc-118">-Type</span></span>
<span data-ttu-id="4b1cc-119">Var olan bir kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="4b1cc-120">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-120">This parameter is required.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1cc-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b1cc-121">-Confirm</span></span>
<span data-ttu-id="4b1cc-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b1cc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b1cc-123">-WhatIf</span></span>
<span data-ttu-id="4b1cc-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b1cc-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b1cc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b1cc-126">CommonParameters</span></span>
<span data-ttu-id="4b1cc-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b1cc-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b1cc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b1cc-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b1cc-129">INPUTS</span></span>

### <span data-ttu-id="4b1cc-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4b1cc-130">None</span></span>
<span data-ttu-id="4b1cc-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4b1cc-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4b1cc-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b1cc-132">OUTPUTS</span></span>

### <span data-ttu-id="4b1cc-133">bool</span><span class="sxs-lookup"><span data-stu-id="4b1cc-133">bool</span></span>

## <span data-ttu-id="4b1cc-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b1cc-134">NOTES</span></span>

## <span data-ttu-id="4b1cc-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b1cc-135">RELATED LINKS</span></span>

[<span data-ttu-id="4b1cc-136">Yeni-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="4b1cc-136">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="4b1cc-137">Get-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="4b1cc-137">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="4b1cc-138">Set-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="4b1cc-138">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

