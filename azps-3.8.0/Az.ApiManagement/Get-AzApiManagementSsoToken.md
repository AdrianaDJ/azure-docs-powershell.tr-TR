---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 25c2439c07c9fe0b611c5b845f56e1de04f4d375
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104655"
---
# <span data-ttu-id="d1711-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="d1711-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="d1711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1711-102">SYNOPSIS</span></span>
<span data-ttu-id="d1711-103">Bir API yönetim hizmetinin dağıtılmış yönetim portalına SSO belirteci içeren bir bağlantı alır.</span><span class="sxs-lookup"><span data-stu-id="d1711-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="d1711-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1711-104">SYNTAX</span></span>

### <span data-ttu-id="d1711-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d1711-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1711-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d1711-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1711-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1711-107">DESCRIPTION</span></span>
<span data-ttu-id="d1711-108">**Get-Azapsananagementssotoken** CMDLET 'ı API yönetim hizmetinin dağıtılmış yönetim portalına çoklu oturum açma (SSO) belirteci içeren bir bağlantı (URL) döndürür.</span><span class="sxs-lookup"><span data-stu-id="d1711-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="d1711-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1711-109">EXAMPLES</span></span>

### <span data-ttu-id="d1711-110">Örnek 1: bir API yönetim hizmetinin SSO belirtecini alma</span><span class="sxs-lookup"><span data-stu-id="d1711-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="d1711-111">Bu komut, bir API yönetim hizmetinin SSO belirtecini alır.</span><span class="sxs-lookup"><span data-stu-id="d1711-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="d1711-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1711-112">PARAMETERS</span></span>

### <span data-ttu-id="d1711-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1711-113">-DefaultProfile</span></span>
<span data-ttu-id="d1711-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1711-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1711-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1711-115">-InputObject</span></span>
<span data-ttu-id="d1711-116">Örnek bir örnek.</span><span class="sxs-lookup"><span data-stu-id="d1711-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="d1711-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d1711-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1711-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="d1711-118">-Name</span></span>
<span data-ttu-id="d1711-119">API yönetim örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1711-119">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1711-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1711-120">-ResourceGroupName</span></span>
<span data-ttu-id="d1711-121">API yönetiminin altında bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1711-121">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1711-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1711-122">CommonParameters</span></span>
<span data-ttu-id="d1711-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1711-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1711-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d1711-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1711-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1711-125">INPUTS</span></span>

### <span data-ttu-id="d1711-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d1711-126">System.String</span></span>

## <span data-ttu-id="d1711-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1711-127">OUTPUTS</span></span>

### <span data-ttu-id="d1711-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d1711-128">System.String</span></span>

## <span data-ttu-id="d1711-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1711-129">NOTES</span></span>

## <span data-ttu-id="d1711-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1711-130">RELATED LINKS</span></span>

[<span data-ttu-id="d1711-131">Get-Azıbir</span><span class="sxs-lookup"><span data-stu-id="d1711-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


