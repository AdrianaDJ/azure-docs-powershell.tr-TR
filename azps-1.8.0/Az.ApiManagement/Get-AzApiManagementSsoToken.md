---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 40c9166ab650f7cb31ac53c55397bb7bc635f6e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751144"
---
# <span data-ttu-id="f6d4c-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="f6d4c-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="f6d4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d4c-103">Bir API yönetim hizmetinin dağıtılmış yönetim portalına SSO belirteci içeren bir bağlantı alır.</span><span class="sxs-lookup"><span data-stu-id="f6d4c-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="f6d4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6d4c-104">SYNTAX</span></span>

```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6d4c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6d4c-105">DESCRIPTION</span></span>
<span data-ttu-id="f6d4c-106">**Get-Azapsananagementssotoken** CMDLET 'ı API yönetim hizmetinin dağıtılmış yönetim portalına çoklu oturum açma (SSO) belirteci içeren bir bağlantı (URL) döndürür.</span><span class="sxs-lookup"><span data-stu-id="f6d4c-106">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="f6d4c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6d4c-107">EXAMPLES</span></span>

### <span data-ttu-id="f6d4c-108">Örnek 1: bir API yönetim hizmetinin SSO belirtecini alma</span><span class="sxs-lookup"><span data-stu-id="f6d4c-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="f6d4c-109">Bu komut, bir API yönetim hizmetinin SSO belirtecini alır.</span><span class="sxs-lookup"><span data-stu-id="f6d4c-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="f6d4c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6d4c-110">PARAMETERS</span></span>

### <span data-ttu-id="f6d4c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d4c-111">-DefaultProfile</span></span>
<span data-ttu-id="f6d4c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6d4c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6d4c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6d4c-113">-Name</span></span>
<span data-ttu-id="f6d4c-114">API yönetim örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6d4c-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="f6d4c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6d4c-115">-ResourceGroupName</span></span>
<span data-ttu-id="f6d4c-116">API yönetiminin altında bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6d4c-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="f6d4c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d4c-117">CommonParameters</span></span>
<span data-ttu-id="f6d4c-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6d4c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d4c-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6d4c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d4c-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6d4c-120">INPUTS</span></span>

### <span data-ttu-id="f6d4c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f6d4c-121">System.String</span></span>

## <span data-ttu-id="f6d4c-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6d4c-122">OUTPUTS</span></span>

### <span data-ttu-id="f6d4c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f6d4c-123">System.String</span></span>

## <span data-ttu-id="f6d4c-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6d4c-124">NOTES</span></span>

## <span data-ttu-id="f6d4c-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6d4c-125">RELATED LINKS</span></span>

[<span data-ttu-id="f6d4c-126">Get-Azıbir</span><span class="sxs-lookup"><span data-stu-id="f6d4c-126">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


