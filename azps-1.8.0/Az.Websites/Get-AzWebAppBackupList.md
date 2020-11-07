---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: fab8973c63e419cdef45fb79a0ad5182c46f2de5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753842"
---
# <span data-ttu-id="da3d8-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="da3d8-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="da3d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da3d8-102">SYNOPSIS</span></span>

## <span data-ttu-id="da3d8-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da3d8-103">SYNTAX</span></span>

### <span data-ttu-id="da3d8-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="da3d8-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da3d8-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="da3d8-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da3d8-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="da3d8-106">DESCRIPTION</span></span>
<span data-ttu-id="da3d8-107">**Get-AzWebAppBackupList** cmdlet 'ı bir Azure Web App yedeklemelerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="da3d8-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="da3d8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da3d8-108">EXAMPLES</span></span>

### <span data-ttu-id="da3d8-109">2</span><span class="sxs-lookup"><span data-stu-id="da3d8-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="da3d8-110">Bu komut, WebApp kaynak grubuyla ilişkilendirilmiş WebApp WebAppStandard ile ilgili bir yedekleme listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="da3d8-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="da3d8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da3d8-111">PARAMETERS</span></span>

### <span data-ttu-id="da3d8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da3d8-112">-DefaultProfile</span></span>
<span data-ttu-id="da3d8-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="da3d8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da3d8-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="da3d8-114">-Name</span></span>
<span data-ttu-id="da3d8-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="da3d8-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da3d8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da3d8-116">-ResourceGroupName</span></span>
<span data-ttu-id="da3d8-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="da3d8-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da3d8-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="da3d8-118">-Slot</span></span>
<span data-ttu-id="da3d8-119">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="da3d8-119">Slot name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da3d8-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="da3d8-120">-WebApp</span></span>
<span data-ttu-id="da3d8-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="da3d8-121">Piped WebApp</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da3d8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da3d8-122">CommonParameters</span></span>
<span data-ttu-id="da3d8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da3d8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da3d8-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da3d8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da3d8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da3d8-125">INPUTS</span></span>

### <span data-ttu-id="da3d8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="da3d8-126">System.String</span></span>

### <span data-ttu-id="da3d8-127">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="da3d8-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="da3d8-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da3d8-128">OUTPUTS</span></span>

### <span data-ttu-id="da3d8-129">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="da3d8-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="da3d8-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da3d8-130">NOTES</span></span>

## <span data-ttu-id="da3d8-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da3d8-131">RELATED LINKS</span></span>
