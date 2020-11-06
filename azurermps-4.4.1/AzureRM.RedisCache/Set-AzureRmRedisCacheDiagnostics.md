---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 103567021d7317a6777ca5fdb01c53d1f9f023a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594182"
---
# <span data-ttu-id="f9b4c-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f9b4c-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="f9b4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b4c-103">Azure Redis Cache 'de tanılamayı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="f9b4c-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9b4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9b4c-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics -ResourceGroupName <String> -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9b4c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9b4c-105">DESCRIPTION</span></span>
<span data-ttu-id="f9b4c-106">**Set-Azurermrediscachediagnosks** cmdlet 'ı Azure Redis önbelleğinin tanılamasını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="f9b4c-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="f9b4c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9b4c-107">EXAMPLES</span></span>

### <span data-ttu-id="f9b4c-108">Örnek 1: tanılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f9b4c-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="f9b4c-109">Bu komut, Azure Redis önbelleğinin tanılamasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="f9b4c-109">This command enables diagnostics for an Azure Redis cache.</span></span>

<span data-ttu-id="f9b4c-110">Bu komut, abonelikler için aynı bölgedeki tüm Azure redin önbelleklerinin tanılama veya depolama hesabını güncellemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="f9b4c-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="f9b4c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9b4c-111">PARAMETERS</span></span>

### <span data-ttu-id="f9b4c-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9b4c-112">-Name</span></span>
<span data-ttu-id="f9b4c-113">Önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9b4c-113">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="f9b4c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b4c-114">-ResourceGroupName</span></span>
<span data-ttu-id="f9b4c-115">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9b4c-115">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="f9b4c-116">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="f9b4c-116">-StorageAccountId</span></span>
<span data-ttu-id="f9b4c-117">Tanılama verilerini depolamak için kullanılan depolama hesabının kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9b4c-117">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="f9b4c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b4c-118">-DefaultProfile</span></span>
<span data-ttu-id="f9b4c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9b4c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9b4c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b4c-120">CommonParameters</span></span>
<span data-ttu-id="f9b4c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9b4c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b4c-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9b4c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b4c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9b4c-123">INPUTS</span></span>

### <span data-ttu-id="f9b4c-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f9b4c-124">None</span></span>

## <span data-ttu-id="f9b4c-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9b4c-125">OUTPUTS</span></span>

### <span data-ttu-id="f9b4c-126">Kılmak</span><span class="sxs-lookup"><span data-stu-id="f9b4c-126">Void</span></span>

## <span data-ttu-id="f9b4c-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9b4c-127">NOTES</span></span>
* <span data-ttu-id="f9b4c-128">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="f9b4c-128">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="f9b4c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9b4c-129">RELATED LINKS</span></span>

[<span data-ttu-id="f9b4c-130">Remove-Azurermrediscachedibelirsiz</span><span class="sxs-lookup"><span data-stu-id="f9b4c-130">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)


