---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 4c6dc810d35feedd0d0d43e0bd3b3efb7c9b6641
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936119"
---
# <span data-ttu-id="d1c51-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1c51-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d1c51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1c51-102">SYNOPSIS</span></span>

## <span data-ttu-id="d1c51-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1c51-103">SYNTAX</span></span>

### <span data-ttu-id="d1c51-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d1c51-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1c51-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d1c51-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1c51-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1c51-106">DESCRIPTION</span></span>
<span data-ttu-id="d1c51-107">**Get-AzWebAppBackupConfiguration** cmdlet 'i, bir Azure Web uygulamasının yedekleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="d1c51-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="d1c51-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1c51-108">EXAMPLES</span></span>

### <span data-ttu-id="d1c51-109">2</span><span class="sxs-lookup"><span data-stu-id="d1c51-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="d1c51-110">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından yedekleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="d1c51-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d1c51-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1c51-111">PARAMETERS</span></span>

### <span data-ttu-id="d1c51-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c51-112">-DefaultProfile</span></span>
<span data-ttu-id="d1c51-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1c51-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1c51-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="d1c51-114">-Name</span></span>
<span data-ttu-id="d1c51-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="d1c51-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c51-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c51-116">-ResourceGroupName</span></span>
<span data-ttu-id="d1c51-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d1c51-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c51-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="d1c51-118">-Slot</span></span>
<span data-ttu-id="d1c51-119">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="d1c51-119">Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c51-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d1c51-120">-WebApp</span></span>
<span data-ttu-id="d1c51-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="d1c51-121">WebApp Name</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c51-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c51-122">CommonParameters</span></span>
<span data-ttu-id="d1c51-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1c51-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c51-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1c51-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c51-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1c51-125">INPUTS</span></span>

### <span data-ttu-id="d1c51-126">Bölge</span><span class="sxs-lookup"><span data-stu-id="d1c51-126">Site</span></span>
<span data-ttu-id="d1c51-127">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d1c51-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d1c51-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1c51-128">OUTPUTS</span></span>

### <span data-ttu-id="d1c51-129">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1c51-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d1c51-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1c51-130">NOTES</span></span>

## <span data-ttu-id="d1c51-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1c51-131">RELATED LINKS</span></span>

