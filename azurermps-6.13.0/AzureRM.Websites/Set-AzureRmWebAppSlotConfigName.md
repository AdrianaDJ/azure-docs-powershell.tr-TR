---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 75c134b162636f94b00cf6692f4e9df120930dcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590768"
---
# <span data-ttu-id="6dd00-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="6dd00-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="6dd00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dd00-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd00-103">Web uygulaması yuva yapılandırma adlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6dd00-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dd00-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6dd00-104">SYNTAX</span></span>

### <span data-ttu-id="6dd00-105">S1</span><span class="sxs-lookup"><span data-stu-id="6dd00-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dd00-106">S2</span><span class="sxs-lookup"><span data-stu-id="6dd00-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dd00-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6dd00-107">DESCRIPTION</span></span>
<span data-ttu-id="6dd00-108">**Set-AzureRmWebAppSlotConfigName** cmdlet 'i yuva ayarları olarak uygulama ayarlarını ve bağlantı dizelerini işaretler</span><span class="sxs-lookup"><span data-stu-id="6dd00-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="6dd00-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6dd00-109">EXAMPLES</span></span>

### <span data-ttu-id="6dd00-110">2</span><span class="sxs-lookup"><span data-stu-id="6dd00-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="6dd00-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için tüm uygulama ayarlarını ve bağlantı dizelerini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6dd00-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="6dd00-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6dd00-112">PARAMETERS</span></span>

### <span data-ttu-id="6dd00-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="6dd00-113">-AppSettingNames</span></span>
<span data-ttu-id="6dd00-114">Uygulama ayarları adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="6dd00-114">App Settings Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd00-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="6dd00-115">-ConnectionStringNames</span></span>
<span data-ttu-id="6dd00-116">Bağlantı dizesi adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="6dd00-116">Connection String Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd00-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd00-117">-DefaultProfile</span></span>
<span data-ttu-id="6dd00-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6dd00-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dd00-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="6dd00-119">-Name</span></span>
<span data-ttu-id="6dd00-120">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="6dd00-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd00-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="6dd00-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="6dd00-122">Tüm uygulama ayar adlarını Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="6dd00-122">Remove All App Setting Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd00-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="6dd00-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="6dd00-124">Tüm bağlantı dizesi adlarını Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="6dd00-124">Remove All Connection String Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd00-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dd00-125">-ResourceGroupName</span></span>
<span data-ttu-id="6dd00-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6dd00-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd00-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6dd00-127">-WebApp</span></span>
<span data-ttu-id="6dd00-128">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="6dd00-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd00-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd00-129">CommonParameters</span></span>
<span data-ttu-id="6dd00-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6dd00-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd00-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dd00-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd00-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6dd00-132">INPUTS</span></span>

### <span data-ttu-id="6dd00-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="6dd00-133">System.String[]</span></span>

### <span data-ttu-id="6dd00-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6dd00-134">System.String</span></span>

### <span data-ttu-id="6dd00-135">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="6dd00-135">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="6dd00-136">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6dd00-136">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="6dd00-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6dd00-137">OUTPUTS</span></span>

### <span data-ttu-id="6dd00-138">Microsoft. Azure. Management. Web sitesi. modeller. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="6dd00-138">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="6dd00-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6dd00-139">NOTES</span></span>

## <span data-ttu-id="6dd00-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6dd00-140">RELATED LINKS</span></span>
