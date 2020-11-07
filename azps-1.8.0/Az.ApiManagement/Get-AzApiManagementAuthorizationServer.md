---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 2624ccad63b2992ef8cae889cea04b849658444e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751168"
---
# <span data-ttu-id="8acab-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8acab-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="8acab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8acab-102">SYNOPSIS</span></span>
<span data-ttu-id="8acab-103">Bir API yönetim yetkilendirme sunucusu alır.</span><span class="sxs-lookup"><span data-stu-id="8acab-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="8acab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8acab-104">SYNTAX</span></span>

### <span data-ttu-id="8acab-105">GetAllAuthorizationServers (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8acab-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8acab-106">Getbyserverıd</span><span class="sxs-lookup"><span data-stu-id="8acab-106">GetByServerId</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8acab-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8acab-107">DESCRIPTION</span></span>
<span data-ttu-id="8acab-108">**Get-Azapsananagementauthorizationserver** cmdlet 'ı tüm Azure API yönetim yetkilendirme sunucularını veya belirtilen yetkilendirme sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="8acab-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="8acab-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8acab-109">EXAMPLES</span></span>

### <span data-ttu-id="8acab-110">Örnek 1: tüm yetkilendirme sunucularını alma</span><span class="sxs-lookup"><span data-stu-id="8acab-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="8acab-111">Bu komut tüm API yönetim yetkilendirme sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="8acab-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="8acab-112">Örnek 2: belirtilen yetkilendirme sunucusunu alma</span><span class="sxs-lookup"><span data-stu-id="8acab-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="8acab-113">Bu komut belirtilen yetkilendirme sunucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="8acab-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="8acab-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8acab-114">PARAMETERS</span></span>

### <span data-ttu-id="8acab-115">-Context</span><span class="sxs-lookup"><span data-stu-id="8acab-115">-Context</span></span>

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

### <span data-ttu-id="8acab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8acab-116">-DefaultProfile</span></span>
<span data-ttu-id="8acab-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8acab-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8acab-118">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="8acab-118">-ServerId</span></span>
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

### <span data-ttu-id="8acab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8acab-119">CommonParameters</span></span>
<span data-ttu-id="8acab-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8acab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8acab-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8acab-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8acab-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8acab-122">INPUTS</span></span>

### <span data-ttu-id="8acab-123">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="8acab-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8acab-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8acab-124">System.String</span></span>

## <span data-ttu-id="8acab-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8acab-125">OUTPUTS</span></span>

### <span data-ttu-id="8acab-126">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="8acab-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="8acab-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8acab-127">NOTES</span></span>

## <span data-ttu-id="8acab-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8acab-128">RELATED LINKS</span></span>

[<span data-ttu-id="8acab-129">Yeni-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="8acab-129">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="8acab-130">Remove-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="8acab-130">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="8acab-131">Set-Azapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="8acab-131">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


