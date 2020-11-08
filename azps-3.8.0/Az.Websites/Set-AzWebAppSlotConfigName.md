---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: a2c57ebe6f85209596628dffe9de88ca260bbafa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098077"
---
# <span data-ttu-id="4f591-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="4f591-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="4f591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f591-102">SYNOPSIS</span></span>
<span data-ttu-id="4f591-103">Web uygulaması yuva yapılandırma adlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="4f591-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="4f591-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f591-104">SYNTAX</span></span>

### <span data-ttu-id="4f591-105">S1</span><span class="sxs-lookup"><span data-stu-id="4f591-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f591-106">S2</span><span class="sxs-lookup"><span data-stu-id="4f591-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f591-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f591-107">DESCRIPTION</span></span>
<span data-ttu-id="4f591-108">**Set-AzWebAppSlotConfigName** cmdlet 'i yuva ayarları olarak uygulama ayarlarını ve bağlantı dizelerini işaretler</span><span class="sxs-lookup"><span data-stu-id="4f591-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="4f591-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f591-109">EXAMPLES</span></span>

### <span data-ttu-id="4f591-110">2</span><span class="sxs-lookup"><span data-stu-id="4f591-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="4f591-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için tüm uygulama ayarlarını ve bağlantı dizelerini kaldırır</span><span class="sxs-lookup"><span data-stu-id="4f591-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="4f591-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f591-112">PARAMETERS</span></span>

### <span data-ttu-id="4f591-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="4f591-113">-AppSettingNames</span></span>
<span data-ttu-id="4f591-114">Uygulama ayarları adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="4f591-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="4f591-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="4f591-115">-ConnectionStringNames</span></span>
<span data-ttu-id="4f591-116">Bağlantı dizesi adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="4f591-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="4f591-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f591-117">-DefaultProfile</span></span>
<span data-ttu-id="4f591-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f591-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f591-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f591-119">-Name</span></span>
<span data-ttu-id="4f591-120">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="4f591-120">WebApp Name</span></span>

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

### <span data-ttu-id="4f591-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="4f591-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="4f591-122">Tüm uygulama ayar adlarını Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="4f591-122">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="4f591-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="4f591-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="4f591-124">Tüm bağlantı dizesi adlarını Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="4f591-124">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="4f591-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f591-125">-ResourceGroupName</span></span>
<span data-ttu-id="4f591-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4f591-126">Resource Group Name</span></span>

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

### <span data-ttu-id="4f591-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4f591-127">-WebApp</span></span>
<span data-ttu-id="4f591-128">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="4f591-128">WebApp Object</span></span>

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

### <span data-ttu-id="4f591-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f591-129">CommonParameters</span></span>
<span data-ttu-id="4f591-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f591-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f591-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f591-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f591-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f591-132">INPUTS</span></span>

### <span data-ttu-id="4f591-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="4f591-133">System.String[]</span></span>

### <span data-ttu-id="4f591-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4f591-134">System.String</span></span>

### <span data-ttu-id="4f591-135">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="4f591-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4f591-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f591-136">OUTPUTS</span></span>

### <span data-ttu-id="4f591-137">Microsoft. Azure. Management. Web sitesi. modeller. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="4f591-137">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="4f591-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f591-138">NOTES</span></span>

## <span data-ttu-id="4f591-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f591-139">RELATED LINKS</span></span>
