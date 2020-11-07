---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: 90da707ce34c191a33a68473f41555a33c0e35b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753534"
---
# <span data-ttu-id="03089-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="03089-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="03089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03089-102">SYNOPSIS</span></span>
<span data-ttu-id="03089-103">Yeni bir önbellek varlığı oluşturur</span><span class="sxs-lookup"><span data-stu-id="03089-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="03089-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03089-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03089-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="03089-105">DESCRIPTION</span></span>
<span data-ttu-id="03089-106">**New-Azapsananagementcache** cmdlet 'ı API Yönetim hizmetinde yeni bir önbellek varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03089-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="03089-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03089-107">EXAMPLES</span></span>

### <span data-ttu-id="03089-108">Örnek 1: yeni bir önbellek varlığı oluşturma</span><span class="sxs-lookup"><span data-stu-id="03089-108">Example 1 : Create a new Cache entity</span></span>
```powershell
PS c:\> New-AzApiManagementCache -Context $context -ConnectionString "teamdemo.redis.cache.windows.net:6380,password=xxxxxx+xxxxx=,ssl=True,abortConnect=False" -Description "Team Cache"

CacheId           : centralus
Description       : Team Cache
ConnectionString  : {{5cc19889e6ed3b0524c3f7d3}}
ResourceId        :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsof
                    t.ApiManagement/service/contoso/caches/centralus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="03089-109">Cmdlet 'ler API yönetim hizmetinin ana konumunda yeni bir önbellek varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03089-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="03089-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03089-110">PARAMETERS</span></span>

### <span data-ttu-id="03089-111">-Azureredisresourceıd</span><span class="sxs-lookup"><span data-stu-id="03089-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="03089-112">Azure Redis Cache örneğinin ARM RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="03089-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="03089-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="03089-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="03089-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="03089-114">-CacheId</span></span>
<span data-ttu-id="03089-115">Yeni önbelleğin tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="03089-115">Identifier of new cache.</span></span>
<span data-ttu-id="03089-116">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="03089-116">This parameter is optional.</span></span>
<span data-ttu-id="03089-117">Belirtilmemişse,.</span><span class="sxs-lookup"><span data-stu-id="03089-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="03089-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="03089-118">-ConnectionString</span></span>
<span data-ttu-id="03089-119">Kırmızı bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="03089-119">Redis Connection String.</span></span>
<span data-ttu-id="03089-120">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="03089-120">This parameter is required.</span></span>

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

### <span data-ttu-id="03089-121">-Context</span><span class="sxs-lookup"><span data-stu-id="03089-121">-Context</span></span>
<span data-ttu-id="03089-122">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="03089-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="03089-123">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="03089-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03089-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03089-124">-DefaultProfile</span></span>
<span data-ttu-id="03089-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03089-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03089-126">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="03089-126">-Description</span></span>
<span data-ttu-id="03089-127">Önbellek açıklaması.</span><span class="sxs-lookup"><span data-stu-id="03089-127">Cache Description.</span></span>
<span data-ttu-id="03089-128">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="03089-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="03089-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="03089-129">-Confirm</span></span>
<span data-ttu-id="03089-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="03089-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03089-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03089-131">-WhatIf</span></span>
<span data-ttu-id="03089-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="03089-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03089-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="03089-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03089-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03089-134">CommonParameters</span></span>
<span data-ttu-id="03089-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03089-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03089-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="03089-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03089-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03089-137">INPUTS</span></span>

### <span data-ttu-id="03089-138">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="03089-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="03089-139">System. String</span><span class="sxs-lookup"><span data-stu-id="03089-139">System.String</span></span>

## <span data-ttu-id="03089-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03089-140">OUTPUTS</span></span>

### <span data-ttu-id="03089-141">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="03089-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="03089-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03089-142">NOTES</span></span>

## <span data-ttu-id="03089-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03089-143">RELATED LINKS</span></span>

[<span data-ttu-id="03089-144">Get-Azapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="03089-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache)

[<span data-ttu-id="03089-145">Set-Azapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="03089-145">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="03089-146">Remove-Azapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="03089-146">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
