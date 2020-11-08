---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: ab00a1fbafc446affd30d7ae06dd0d48f0f0d04d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936060"
---
# <span data-ttu-id="11241-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="11241-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="11241-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11241-102">SYNOPSIS</span></span>
<span data-ttu-id="11241-103">Web uygulaması yuva yapılandırma adlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="11241-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="11241-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11241-104">SYNTAX</span></span>

### <span data-ttu-id="11241-105">S1</span><span class="sxs-lookup"><span data-stu-id="11241-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11241-106">S2</span><span class="sxs-lookup"><span data-stu-id="11241-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11241-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="11241-107">DESCRIPTION</span></span>
<span data-ttu-id="11241-108">**Set-AzWebAppSlotConfigName** cmdlet 'i yuva ayarları olarak uygulama ayarlarını ve bağlantı dizelerini işaretler</span><span class="sxs-lookup"><span data-stu-id="11241-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="11241-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11241-109">EXAMPLES</span></span>

### <span data-ttu-id="11241-110">2</span><span class="sxs-lookup"><span data-stu-id="11241-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="11241-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için tüm uygulama ayarlarını ve bağlantı dizelerini kaldırır</span><span class="sxs-lookup"><span data-stu-id="11241-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="11241-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11241-112">PARAMETERS</span></span>

### <span data-ttu-id="11241-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="11241-113">-AppSettingNames</span></span>
<span data-ttu-id="11241-114">Uygulama ayarları adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="11241-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="11241-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="11241-115">-ConnectionStringNames</span></span>
<span data-ttu-id="11241-116">Bağlantı dizesi adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="11241-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="11241-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11241-117">-DefaultProfile</span></span>
<span data-ttu-id="11241-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11241-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11241-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="11241-119">-Name</span></span>
<span data-ttu-id="11241-120">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="11241-120">WebApp Name</span></span>

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

### <span data-ttu-id="11241-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="11241-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="11241-122">Tüm uygulama ayar adlarını Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="11241-122">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="11241-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="11241-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="11241-124">Tüm bağlantı dizesi adlarını Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="11241-124">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="11241-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11241-125">-ResourceGroupName</span></span>
<span data-ttu-id="11241-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="11241-126">Resource Group Name</span></span>

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

### <span data-ttu-id="11241-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="11241-127">-WebApp</span></span>
<span data-ttu-id="11241-128">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="11241-128">WebApp Object</span></span>

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

### <span data-ttu-id="11241-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11241-129">CommonParameters</span></span>
<span data-ttu-id="11241-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11241-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11241-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11241-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11241-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11241-132">INPUTS</span></span>

### <span data-ttu-id="11241-133">Bölge</span><span class="sxs-lookup"><span data-stu-id="11241-133">Site</span></span>
<span data-ttu-id="11241-134">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="11241-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="11241-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11241-135">OUTPUTS</span></span>

## <span data-ttu-id="11241-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11241-136">NOTES</span></span>

## <span data-ttu-id="11241-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11241-137">RELATED LINKS</span></span>
