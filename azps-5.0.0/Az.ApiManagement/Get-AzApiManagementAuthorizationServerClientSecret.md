---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: 19e49269a4ae07b39e7a2795636e51df75b54905
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324076"
---
# <span data-ttu-id="1c6da-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="1c6da-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="1c6da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c6da-102">SYNOPSIS</span></span>
<span data-ttu-id="1c6da-103">API yönetim yetkilendirme sunucusu istemci parolasını alır.</span><span class="sxs-lookup"><span data-stu-id="1c6da-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="1c6da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c6da-104">SYNTAX</span></span>

### <span data-ttu-id="1c6da-105">ContextParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1c6da-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c6da-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="1c6da-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c6da-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c6da-107">DESCRIPTION</span></span>
<span data-ttu-id="1c6da-108">**Get-Azapsananagementauthorizationserverclientsecret** cmdlet 'ı Azure API yönetim yetkilendirme sunucusunun istemci gizliliğini alır.</span><span class="sxs-lookup"><span data-stu-id="1c6da-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="1c6da-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c6da-109">EXAMPLES</span></span>

### <span data-ttu-id="1c6da-110">Örnek 1: kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="1c6da-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="1c6da-111">Bu komut, belirtilen yetkilendirme sunucusu gizli gizliliğini alır.</span><span class="sxs-lookup"><span data-stu-id="1c6da-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="1c6da-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c6da-112">PARAMETERS</span></span>

### <span data-ttu-id="1c6da-113">-Context</span><span class="sxs-lookup"><span data-stu-id="1c6da-113">-Context</span></span>
<span data-ttu-id="1c6da-114">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="1c6da-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1c6da-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1c6da-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c6da-116">-DefaultProfile</span></span>
<span data-ttu-id="1c6da-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1c6da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c6da-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1c6da-118">-ResourceId</span></span>
<span data-ttu-id="1c6da-119">Yetkilendirme sunucusunun ARM kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="1c6da-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="1c6da-120">Belirtilirse, tanımlayıcı tarafından yetkilendirme sunucusunu bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="1c6da-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="1c6da-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1c6da-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6da-122">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="1c6da-122">-ServerId</span></span>
<span data-ttu-id="1c6da-123">Yetkilendirme sunucusunun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="1c6da-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="1c6da-124">Belirtilmişse, kimlik doğrulama sunucusunu tanımlayıcı tarafından bulur.</span><span class="sxs-lookup"><span data-stu-id="1c6da-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="1c6da-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="1c6da-125">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6da-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c6da-126">CommonParameters</span></span>
<span data-ttu-id="1c6da-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c6da-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c6da-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1c6da-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c6da-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c6da-129">INPUTS</span></span>

### <span data-ttu-id="1c6da-130">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="1c6da-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1c6da-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1c6da-131">System.String</span></span>

## <span data-ttu-id="1c6da-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c6da-132">OUTPUTS</span></span>

### <span data-ttu-id="1c6da-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementclientsecret</span><span class="sxs-lookup"><span data-stu-id="1c6da-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="1c6da-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c6da-134">NOTES</span></span>

## <span data-ttu-id="1c6da-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c6da-135">RELATED LINKS</span></span>
