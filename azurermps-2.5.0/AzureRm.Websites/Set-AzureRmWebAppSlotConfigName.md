---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslotconfigname
schema: 2.0.0
ms.openlocfilehash: 39c3ce693a1ee17a5b547c027ab9165388fe10f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939658"
---
# <span data-ttu-id="ea0e0-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="ea0e0-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="ea0e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0e0-103">Web uygulaması yuva yapılandırma adlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ea0e0-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea0e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea0e0-104">SYNTAX</span></span>

### <span data-ttu-id="ea0e0-105">S1</span><span class="sxs-lookup"><span data-stu-id="ea0e0-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea0e0-106">S2</span><span class="sxs-lookup"><span data-stu-id="ea0e0-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea0e0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea0e0-107">DESCRIPTION</span></span>
<span data-ttu-id="ea0e0-108">**Set-AzureRmWebAppSlotConfigName** cmdlet 'i yuva ayarları olarak uygulama ayarlarını ve bağlantı dizelerini işaretler</span><span class="sxs-lookup"><span data-stu-id="ea0e0-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="ea0e0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea0e0-109">EXAMPLES</span></span>

### <span data-ttu-id="ea0e0-110">2</span><span class="sxs-lookup"><span data-stu-id="ea0e0-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="ea0e0-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için tüm uygulama ayarlarını ve bağlantı dizelerini kaldırır</span><span class="sxs-lookup"><span data-stu-id="ea0e0-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ea0e0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea0e0-112">PARAMETERS</span></span>

### <span data-ttu-id="ea0e0-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="ea0e0-113">-AppSettingNames</span></span>
<span data-ttu-id="ea0e0-114">Uygulama ayarları adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="ea0e0-114">App Settings Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0e0-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="ea0e0-115">-ConnectionStringNames</span></span>
<span data-ttu-id="ea0e0-116">Bağlantı dizesi adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="ea0e0-116">Connection String Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0e0-117">-DefaultProfile</span></span>
<span data-ttu-id="ea0e0-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea0e0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0e0-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea0e0-119">-Name</span></span>
<span data-ttu-id="ea0e0-120">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="ea0e0-120">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0e0-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="ea0e0-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="ea0e0-122">Tüm uygulama ayar adlarını Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="ea0e0-122">Remove All App Setting Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0e0-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="ea0e0-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="ea0e0-124">Tüm bağlantı dizesi adlarını Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="ea0e0-124">Remove All Connection String Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0e0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea0e0-125">-ResourceGroupName</span></span>
<span data-ttu-id="ea0e0-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ea0e0-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0e0-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ea0e0-127">-WebApp</span></span>
<span data-ttu-id="ea0e0-128">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="ea0e0-128">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0e0-129">CommonParameters</span></span>
<span data-ttu-id="ea0e0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea0e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0e0-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea0e0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0e0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea0e0-132">INPUTS</span></span>

### <span data-ttu-id="ea0e0-133">Bölge</span><span class="sxs-lookup"><span data-stu-id="ea0e0-133">Site</span></span>
<span data-ttu-id="ea0e0-134">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ea0e0-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ea0e0-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea0e0-135">OUTPUTS</span></span>

## <span data-ttu-id="ea0e0-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea0e0-136">NOTES</span></span>

## <span data-ttu-id="ea0e0-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea0e0-137">RELATED LINKS</span></span>

