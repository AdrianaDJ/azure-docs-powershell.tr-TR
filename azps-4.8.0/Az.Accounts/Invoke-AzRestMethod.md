---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275115"
---
# <span data-ttu-id="0cda5-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="0cda5-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="0cda5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cda5-102">SYNOPSIS</span></span>
<span data-ttu-id="0cda5-103">Yalnızca Azure Kaynak Yönetimi uç noktasına HTTP isteği oluşturma ve gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="0cda5-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="0cda5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0cda5-104">SYNTAX</span></span>

### <span data-ttu-id="0cda5-105">ByPath (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0cda5-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cda5-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="0cda5-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cda5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0cda5-107">DESCRIPTION</span></span>
<span data-ttu-id="0cda5-108">Yalnızca Azure Kaynak Yönetimi uç noktasına HTTP isteği oluşturma ve gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="0cda5-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="0cda5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0cda5-109">EXAMPLES</span></span>

### <span data-ttu-id="0cda5-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0cda5-110">Example 1</span></span>
```powershell
Invoke-AzRestMethod -Path "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}?api-version={API}" -Method GET

Headers    : {[Cache-Control, System.String[]], [Pragma, System.String[]], [x-ms-request-id, System.String[]], [Strict-Transport-Security, System.String[]]…}
Version    : 1.1
StatusCode : 200
Method     : GET
Content    : {
               "properties": {
                 "source": "Azure",
                 "customerId": "{customerId}",
                 "provisioningState": "Succeeded",
                 "sku": {
                   "name": "pergb2018",
                   "maxCapacityReservationLevel": 3000,
                   "lastSkuUpdate": "Mon, 25 May 2020 11:10:01 GMT"
                 },
                 "retentionInDays": 30,
                 "features": {
                   "legacy": 0,
                   "searchVersion": 1,
                   "enableLogAccessUsingOnlyResourcePermissions": true
                 },
                 "workspaceCapping": {
                   "dailyQuotaGb": -1.0,
                   "quotaNextResetTime": "Thu, 18 Jun 2020 05:00:00 GMT",
                   "dataIngestionStatus": "RespectQuota"
                 },
                 "enableFailover": false,
                 "publicNetworkAccessForIngestion": "Enabled",
                 "publicNetworkAccessForQuery": "Enabled",
                 "createdDate": "Mon, 25 May 2020 11:10:01 GMT",
                 "modifiedDate": "Mon, 25 May 2020 11:10:02 GMT"
               },
               "id": "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}",
               "name": "{workspace}",
               "type": "Microsoft.OperationalInsights/workspaces",
               "location": "eastasia",
               "tags": {}
             }
```

<span data-ttu-id="0cda5-111">Log Analytics çalışma alanını yola göre alma</span><span class="sxs-lookup"><span data-stu-id="0cda5-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="0cda5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0cda5-112">PARAMETERS</span></span>

### <span data-ttu-id="0cda5-113">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="0cda5-113">-ApiVersion</span></span>
<span data-ttu-id="0cda5-114">API sürümü</span><span class="sxs-lookup"><span data-stu-id="0cda5-114">Api Version</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cda5-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="0cda5-115">-AsJob</span></span>
<span data-ttu-id="0cda5-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0cda5-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cda5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cda5-117">-DefaultProfile</span></span>
<span data-ttu-id="0cda5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0cda5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cda5-119">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="0cda5-119">-Method</span></span>
<span data-ttu-id="0cda5-120">Http yöntemi</span><span class="sxs-lookup"><span data-stu-id="0cda5-120">Http Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cda5-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="0cda5-121">-Name</span></span>
<span data-ttu-id="0cda5-122">Hedef kaynak adının listesi</span><span class="sxs-lookup"><span data-stu-id="0cda5-122">list of Target Resource Name</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cda5-123">-Yol</span><span class="sxs-lookup"><span data-stu-id="0cda5-123">-Path</span></span>
<span data-ttu-id="0cda5-124">Hedef yol</span><span class="sxs-lookup"><span data-stu-id="0cda5-124">Target Path</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cda5-125">-Yük</span><span class="sxs-lookup"><span data-stu-id="0cda5-125">-Payload</span></span>
<span data-ttu-id="0cda5-126">JSON biçimi yükü</span><span class="sxs-lookup"><span data-stu-id="0cda5-126">JSON format payload</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cda5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cda5-127">-ResourceGroupName</span></span>
<span data-ttu-id="0cda5-128">Hedef kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0cda5-128">Target Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cda5-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="0cda5-129">-ResourceProviderName</span></span>
<span data-ttu-id="0cda5-130">Hedef kaynak sağlayıcısı adı</span><span class="sxs-lookup"><span data-stu-id="0cda5-130">Target Resource Provider Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cda5-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0cda5-131">-ResourceType</span></span>
<span data-ttu-id="0cda5-132">Hedef kaynak türü listesi</span><span class="sxs-lookup"><span data-stu-id="0cda5-132">List of Target Resource Type</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cda5-133">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0cda5-133">-SubscriptionId</span></span>
<span data-ttu-id="0cda5-134">Hedef abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="0cda5-134">Target Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cda5-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="0cda5-135">-Confirm</span></span>
<span data-ttu-id="0cda5-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0cda5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cda5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cda5-137">-WhatIf</span></span>
<span data-ttu-id="0cda5-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0cda5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cda5-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0cda5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cda5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cda5-140">CommonParameters</span></span>
<span data-ttu-id="0cda5-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0cda5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cda5-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0cda5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cda5-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0cda5-143">INPUTS</span></span>

### <span data-ttu-id="0cda5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0cda5-144">System.string</span></span>

## <span data-ttu-id="0cda5-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0cda5-145">OUTPUTS</span></span>

### <span data-ttu-id="0cda5-146">Microsoft. Azure. Commands. Profile. modeller. PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="0cda5-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="0cda5-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0cda5-147">NOTES</span></span>

## <span data-ttu-id="0cda5-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0cda5-148">RELATED LINKS</span></span>
