---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 2e18be1721f68a0e1223bf45b9ca2e637c05a378
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591475"
---
# <span data-ttu-id="73164-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="73164-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="73164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73164-102">SYNOPSIS</span></span>
<span data-ttu-id="73164-103">Bir API yönetim yetkilendirme sunucusu alır.</span><span class="sxs-lookup"><span data-stu-id="73164-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73164-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73164-104">SYNTAX</span></span>

### <span data-ttu-id="73164-105">GetAllAuthorizationServers (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="73164-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73164-106">Getbyserverıd</span><span class="sxs-lookup"><span data-stu-id="73164-106">GetByServerId</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73164-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="73164-107">DESCRIPTION</span></span>
<span data-ttu-id="73164-108">**Get-Azurermapımanagementauthorizationserver** cmdlet 'ı tüm Azure API yönetim yetkilendirme sunucularını veya belirtilen yetkilendirme sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="73164-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="73164-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73164-109">EXAMPLES</span></span>

### <span data-ttu-id="73164-110">Örnek 1: tüm yetkilendirme sunucularını alma</span><span class="sxs-lookup"><span data-stu-id="73164-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="73164-111">Bu komut tüm API yönetim yetkilendirme sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="73164-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="73164-112">Örnek 2: belirtilen yetkilendirme sunucusunu alma</span><span class="sxs-lookup"><span data-stu-id="73164-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="73164-113">Bu komut belirtilen yetkilendirme sunucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="73164-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="73164-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73164-114">PARAMETERS</span></span>

### <span data-ttu-id="73164-115">-Context</span><span class="sxs-lookup"><span data-stu-id="73164-115">-Context</span></span>

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

### <span data-ttu-id="73164-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73164-116">-DefaultProfile</span></span>
<span data-ttu-id="73164-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73164-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73164-118">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="73164-118">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByServerId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73164-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73164-119">CommonParameters</span></span>
<span data-ttu-id="73164-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73164-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73164-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73164-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73164-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73164-122">INPUTS</span></span>

### <span data-ttu-id="73164-123">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="73164-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="73164-124">System. String</span><span class="sxs-lookup"><span data-stu-id="73164-124">System.String</span></span>

## <span data-ttu-id="73164-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73164-125">OUTPUTS</span></span>

### <span data-ttu-id="73164-126">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="73164-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="73164-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73164-127">NOTES</span></span>

## <span data-ttu-id="73164-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73164-128">RELATED LINKS</span></span>

[<span data-ttu-id="73164-129">Yeni-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="73164-129">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="73164-130">Remove-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="73164-130">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="73164-131">Set-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="73164-131">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


