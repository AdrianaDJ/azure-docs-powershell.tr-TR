---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 3ed7bd25c394c2bef5cb3636a4f8c238f45a3558
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586864"
---
# <span data-ttu-id="c246f-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="c246f-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="c246f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c246f-102">SYNOPSIS</span></span>
<span data-ttu-id="c246f-103">Web uygulaması yuva yapılandırma adlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="c246f-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c246f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c246f-104">SYNTAX</span></span>

### <span data-ttu-id="c246f-105">S1</span><span class="sxs-lookup"><span data-stu-id="c246f-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c246f-106">S2</span><span class="sxs-lookup"><span data-stu-id="c246f-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c246f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c246f-107">DESCRIPTION</span></span>
<span data-ttu-id="c246f-108">**Set-AzureRmWebAppSlotConfigName** cmdlet 'i yuva ayarları olarak uygulama ayarlarını ve bağlantı dizelerini işaretler</span><span class="sxs-lookup"><span data-stu-id="c246f-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="c246f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c246f-109">EXAMPLES</span></span>

### <span data-ttu-id="c246f-110">2</span><span class="sxs-lookup"><span data-stu-id="c246f-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="c246f-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için tüm uygulama ayarlarını ve bağlantı dizelerini kaldırır</span><span class="sxs-lookup"><span data-stu-id="c246f-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c246f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c246f-112">PARAMETERS</span></span>

### <span data-ttu-id="c246f-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="c246f-113">-AppSettingNames</span></span>
<span data-ttu-id="c246f-114">Uygulama ayarları adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="c246f-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="c246f-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="c246f-115">-ConnectionStringNames</span></span>
<span data-ttu-id="c246f-116">Bağlantı dizesi adları dize dizisi</span><span class="sxs-lookup"><span data-stu-id="c246f-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="c246f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c246f-117">-Name</span></span>
<span data-ttu-id="c246f-118">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="c246f-118">WebApp Name</span></span>

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

### <span data-ttu-id="c246f-119">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="c246f-119">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="c246f-120">Tüm uygulama ayar adlarını Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="c246f-120">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="c246f-121">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="c246f-121">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="c246f-122">Tüm bağlantı dizesi adlarını Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="c246f-122">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="c246f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c246f-123">-ResourceGroupName</span></span>
<span data-ttu-id="c246f-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c246f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c246f-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c246f-125">-WebApp</span></span>
<span data-ttu-id="c246f-126">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="c246f-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c246f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c246f-127">-DefaultProfile</span></span>
<span data-ttu-id="c246f-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c246f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c246f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c246f-129">CommonParameters</span></span>
<span data-ttu-id="c246f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c246f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c246f-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c246f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c246f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c246f-132">INPUTS</span></span>

### <span data-ttu-id="c246f-133">Bölge</span><span class="sxs-lookup"><span data-stu-id="c246f-133">Site</span></span>
<span data-ttu-id="c246f-134">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c246f-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c246f-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c246f-135">OUTPUTS</span></span>

## <span data-ttu-id="c246f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c246f-136">NOTES</span></span>

## <span data-ttu-id="c246f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c246f-137">RELATED LINKS</span></span>

