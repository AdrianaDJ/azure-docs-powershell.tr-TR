---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109897"
---
# <span data-ttu-id="17341-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="17341-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="17341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17341-102">SYNOPSIS</span></span>
<span data-ttu-id="17341-103">Var olan ağ geçitindeki anahtarları alır</span><span class="sxs-lookup"><span data-stu-id="17341-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="17341-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17341-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17341-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="17341-105">DESCRIPTION</span></span>
<span data-ttu-id="17341-106">**Get-Azapsananagementgatewaykey** cmdlet 'ı mevcut ağ geçitindeki anahtarları alır</span><span class="sxs-lookup"><span data-stu-id="17341-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="17341-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17341-107">EXAMPLES</span></span>

### <span data-ttu-id="17341-108">Örnek 2: KIMLIĞE göre ağ geçidi alma</span><span class="sxs-lookup"><span data-stu-id="17341-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="17341-109">Bu komut bir "0123456789" ağ geçidi için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="17341-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="17341-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17341-110">PARAMETERS</span></span>

### <span data-ttu-id="17341-111">-Context</span><span class="sxs-lookup"><span data-stu-id="17341-111">-Context</span></span>
<span data-ttu-id="17341-112">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="17341-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="17341-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="17341-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17341-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17341-114">-DefaultProfile</span></span>
<span data-ttu-id="17341-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17341-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17341-116">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="17341-116">-GatewayId</span></span>
<span data-ttu-id="17341-117">Ağ Geçidi tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="17341-117">Gateway identifier.</span></span>
<span data-ttu-id="17341-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="17341-118">This parameter is required.</span></span>

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

### <span data-ttu-id="17341-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17341-119">CommonParameters</span></span>
<span data-ttu-id="17341-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17341-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17341-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="17341-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17341-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17341-122">INPUTS</span></span>

### <span data-ttu-id="17341-123">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="17341-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="17341-124">System. String</span><span class="sxs-lookup"><span data-stu-id="17341-124">System.String</span></span>

## <span data-ttu-id="17341-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17341-125">OUTPUTS</span></span>

### <span data-ttu-id="17341-126">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgatewaykey</span><span class="sxs-lookup"><span data-stu-id="17341-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="17341-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17341-127">NOTES</span></span>

## <span data-ttu-id="17341-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17341-128">RELATED LINKS</span></span>
