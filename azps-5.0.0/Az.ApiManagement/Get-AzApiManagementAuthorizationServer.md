---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324082"
---
# <span data-ttu-id="008b5-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="008b5-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="008b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="008b5-102">SYNOPSIS</span></span>
<span data-ttu-id="008b5-103">Bir API yönetim yetkilendirme sunucusu alır.</span><span class="sxs-lookup"><span data-stu-id="008b5-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="008b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="008b5-104">SYNTAX</span></span>

### <span data-ttu-id="008b5-105">ContextParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="008b5-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="008b5-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="008b5-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="008b5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="008b5-107">DESCRIPTION</span></span>
<span data-ttu-id="008b5-108">**Get-Azapsananagementauthorizationserver** cmdlet 'ı tüm Azure API yönetim yetkilendirme sunucularını veya belirtilen yetkilendirme sunucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="008b5-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="008b5-109">ClientSecret, sonuç ayrıntılarına eklenmeyecek.</span><span class="sxs-lookup"><span data-stu-id="008b5-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="008b5-110">İstemci gizliliğini almak için **Get-Azapsananagementauthorizationserverclientsecret** kullanın.</span><span class="sxs-lookup"><span data-stu-id="008b5-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="008b5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="008b5-111">EXAMPLES</span></span>

### <span data-ttu-id="008b5-112">Örnek 1: tüm yetkilendirme sunucularını alma</span><span class="sxs-lookup"><span data-stu-id="008b5-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="008b5-113">Bu komut tüm API yönetim yetkilendirme sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="008b5-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="008b5-114">Örnek 2: belirtilen yetkilendirme sunucusunu alma</span><span class="sxs-lookup"><span data-stu-id="008b5-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="008b5-115">Bu komut belirtilen yetkilendirme sunucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="008b5-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="008b5-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="008b5-116">PARAMETERS</span></span>

### <span data-ttu-id="008b5-117">-Context</span><span class="sxs-lookup"><span data-stu-id="008b5-117">-Context</span></span>

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

### <span data-ttu-id="008b5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008b5-118">-DefaultProfile</span></span>
<span data-ttu-id="008b5-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="008b5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="008b5-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="008b5-120">-ResourceId</span></span>
<span data-ttu-id="008b5-121">Yetkilendirme sunucusunun ARM kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="008b5-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="008b5-122">Belirtilirse, tanımlayıcı tarafından yetkilendirme sunucusunu bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="008b5-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="008b5-123">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="008b5-123">This parameter is required.</span></span>

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

### <span data-ttu-id="008b5-124">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="008b5-124">-ServerId</span></span>
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

### <span data-ttu-id="008b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008b5-125">CommonParameters</span></span>
<span data-ttu-id="008b5-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="008b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008b5-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="008b5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008b5-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="008b5-128">INPUTS</span></span>

### <span data-ttu-id="008b5-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="008b5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="008b5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="008b5-130">System.String</span></span>

## <span data-ttu-id="008b5-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="008b5-131">OUTPUTS</span></span>

### <span data-ttu-id="008b5-132">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="008b5-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="008b5-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="008b5-133">NOTES</span></span>

## <span data-ttu-id="008b5-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="008b5-134">RELATED LINKS</span></span>

[<span data-ttu-id="008b5-135">Yeni-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="008b5-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="008b5-136">Remove-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="008b5-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="008b5-137">Set-Azapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="008b5-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


