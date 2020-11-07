---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 8b8ac352819b9b3ec7cd655501c5bf8cfbba6816
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753573"
---
# <span data-ttu-id="48dc2-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="48dc2-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="48dc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="48dc2-103">Bir API yönetim hizmetinin dağıtılmış yönetim portalına SSO belirteci içeren bir bağlantı alır.</span><span class="sxs-lookup"><span data-stu-id="48dc2-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="48dc2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48dc2-104">SYNTAX</span></span>

### <span data-ttu-id="48dc2-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="48dc2-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48dc2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="48dc2-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48dc2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="48dc2-107">DESCRIPTION</span></span>
<span data-ttu-id="48dc2-108">**Get-Azapsananagementssotoken** CMDLET 'ı API yönetim hizmetinin dağıtılmış yönetim portalına çoklu oturum açma (SSO) belirteci içeren bir bağlantı (URL) döndürür.</span><span class="sxs-lookup"><span data-stu-id="48dc2-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="48dc2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48dc2-109">EXAMPLES</span></span>

### <span data-ttu-id="48dc2-110">Örnek 1: bir API yönetim hizmetinin SSO belirtecini alma</span><span class="sxs-lookup"><span data-stu-id="48dc2-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="48dc2-111">Bu komut, bir API yönetim hizmetinin SSO belirtecini alır.</span><span class="sxs-lookup"><span data-stu-id="48dc2-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="48dc2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48dc2-112">PARAMETERS</span></span>

### <span data-ttu-id="48dc2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48dc2-113">-DefaultProfile</span></span>
<span data-ttu-id="48dc2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48dc2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48dc2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48dc2-115">-InputObject</span></span>
<span data-ttu-id="48dc2-116">Örnek bir örnek.</span><span class="sxs-lookup"><span data-stu-id="48dc2-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="48dc2-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="48dc2-117">This parameter is required.</span></span>

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

### <span data-ttu-id="48dc2-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="48dc2-118">-Name</span></span>
<span data-ttu-id="48dc2-119">API yönetim örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48dc2-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="48dc2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48dc2-120">-ResourceGroupName</span></span>
<span data-ttu-id="48dc2-121">API yönetiminin altında bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48dc2-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="48dc2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48dc2-122">CommonParameters</span></span>
<span data-ttu-id="48dc2-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48dc2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48dc2-124">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="48dc2-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48dc2-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48dc2-125">INPUTS</span></span>

### <span data-ttu-id="48dc2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="48dc2-126">System.String</span></span>

## <span data-ttu-id="48dc2-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48dc2-127">OUTPUTS</span></span>

### <span data-ttu-id="48dc2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="48dc2-128">System.String</span></span>

## <span data-ttu-id="48dc2-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48dc2-129">NOTES</span></span>

## <span data-ttu-id="48dc2-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48dc2-130">RELATED LINKS</span></span>

[<span data-ttu-id="48dc2-131">Get-Azıbir</span><span class="sxs-lookup"><span data-stu-id="48dc2-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

