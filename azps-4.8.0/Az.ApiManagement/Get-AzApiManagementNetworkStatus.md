---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnetworkstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
ms.openlocfilehash: 5ba351ab1a5102acc1855e13821650b8ce1b4373
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108026"
---
# <span data-ttu-id="770d8-101">Get-AzApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="770d8-101">Get-AzApiManagementNetworkStatus</span></span>

## <span data-ttu-id="770d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770d8-102">SYNOPSIS</span></span>
<span data-ttu-id="770d8-103">API yönetim hizmetinin bulut hizmetinin içinde dayandığı dış kaynaklara bağlantı durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="770d8-103">Gets the Connectivity Status to the external resources on which the Api Management service depends from inside the Cloud Service.</span></span> <span data-ttu-id="770d8-104">Bu, DNS sunucularını CloudService 'e görünür olarak da döndürür.</span><span class="sxs-lookup"><span data-stu-id="770d8-104">This also returns the DNS Servers as visible to the CloudService.</span></span>

## <span data-ttu-id="770d8-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="770d8-105">SYNTAX</span></span>

### <span data-ttu-id="770d8-106">ByInputObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="770d8-106">ByInputObject (Default)</span></span>
```
Get-AzApiManagementNetworkStatus -ApiManagementObject <PsApiManagement> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770d8-107">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="770d8-107">ExpandedParameter</span></span>
```
Get-AzApiManagementNetworkStatus -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="770d8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="770d8-108">DESCRIPTION</span></span>
<span data-ttu-id="770d8-109">API yönetim hizmetlerinin ağ durumunu alır</span><span class="sxs-lookup"><span data-stu-id="770d8-109">Gets the Network status of their Api Management service</span></span>

## <span data-ttu-id="770d8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="770d8-110">EXAMPLES</span></span>

### <span data-ttu-id="770d8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="770d8-111">Example 1</span></span>
```powershell
PS D:\github\azure-powershell> Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice

Location DnsServers      ConnectivityStatus
-------- ----------      ------------------
West US  {168.63.129.16} {apimgmtstaoonqs7wwzjosky.blob.core.windows.net, apimgmtstaoonqs7wwzjosky.file.core.windows.net, apimgmtstaoonqs7wwzjosky.queue.core.windows.net, apimgmtstaoonqs7wwzjosk...


PS D:\github\azure-powershell> $networkStatus = Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice
PS D:\github\azure-powershell> $networkStatus.ConnectivityStatus


Name             : apimgmtstaoonqs7wwzjosky.blob.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : apimgmtstaoonqs7wwzjosky.file.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.queue.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.table.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : bx9gltecfv.database.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:41 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : https://prod3.metrics.nsatc.net:1886/RecoveryService
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:07:11 PM
LastStatusChange : 4/29/2019 1:31:30 PM

Name             : prod.warmpath.msftcloudes.com
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : Scm
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:04:27 PM
LastStatusChange : 4/30/2019 11:16:20 PM
```

<span data-ttu-id="770d8-112">Hangi farklı kaynağın bağlantı durumunu alır ve bu servisin bağlı olduğu farklı kaynaklar.</span><span class="sxs-lookup"><span data-stu-id="770d8-112">Gets the connectivity status of the different resources on which ApiManagement service depends upon.</span></span>

## <span data-ttu-id="770d8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="770d8-113">PARAMETERS</span></span>

### <span data-ttu-id="770d8-114">-Apsananagementobject</span><span class="sxs-lookup"><span data-stu-id="770d8-114">-ApiManagementObject</span></span>
<span data-ttu-id="770d8-115">Örnek bir örnek.</span><span class="sxs-lookup"><span data-stu-id="770d8-115">Instance of PsApiManagement.</span></span> <span data-ttu-id="770d8-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="770d8-116">This parameter is required.</span></span>

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

### <span data-ttu-id="770d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770d8-117">-DefaultProfile</span></span>
<span data-ttu-id="770d8-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="770d8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770d8-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="770d8-119">-Location</span></span>
<span data-ttu-id="770d8-120">API yönetim hizmetinin konumu.</span><span class="sxs-lookup"><span data-stu-id="770d8-120">Location of the API Management Service.</span></span>

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

### <span data-ttu-id="770d8-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="770d8-121">-Name</span></span>
<span data-ttu-id="770d8-122">API yönetiminin adı.</span><span class="sxs-lookup"><span data-stu-id="770d8-122">Name of API Management.</span></span>

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

### <span data-ttu-id="770d8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770d8-123">-ResourceGroupName</span></span>
<span data-ttu-id="770d8-124">API yönetiminin altındaki kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="770d8-124">Name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="770d8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770d8-125">CommonParameters</span></span>
<span data-ttu-id="770d8-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="770d8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770d8-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="770d8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770d8-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="770d8-128">INPUTS</span></span>

### <span data-ttu-id="770d8-129">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="770d8-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="770d8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="770d8-130">System.String</span></span>

## <span data-ttu-id="770d8-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="770d8-131">OUTPUTS</span></span>

### <span data-ttu-id="770d8-132">Microsoft. Azure. Commands. apsananad</span><span class="sxs-lookup"><span data-stu-id="770d8-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span></span>

## <span data-ttu-id="770d8-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="770d8-133">NOTES</span></span>

## <span data-ttu-id="770d8-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="770d8-134">RELATED LINKS</span></span>
