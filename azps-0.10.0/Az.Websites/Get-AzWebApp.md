---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: f86e0f18c7d793b5876a48c39b56b11c14b17546
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936121"
---
# <span data-ttu-id="555d4-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="555d4-101">Get-AzWebApp</span></span>

## <span data-ttu-id="555d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="555d4-102">SYNOPSIS</span></span>
<span data-ttu-id="555d4-103">Belirtilen kaynak grubundaki Azure Web uygulamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="555d4-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="555d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="555d4-104">SYNTAX</span></span>

### <span data-ttu-id="555d4-105">S1</span><span class="sxs-lookup"><span data-stu-id="555d4-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="555d4-106">S2</span><span class="sxs-lookup"><span data-stu-id="555d4-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="555d4-107">S3</span><span class="sxs-lookup"><span data-stu-id="555d4-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="555d4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="555d4-108">DESCRIPTION</span></span>
<span data-ttu-id="555d4-109">**Get-AzWebApp** cmdlet 'ı bir Azure Web App hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="555d4-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="555d4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="555d4-110">EXAMPLES</span></span>

### <span data-ttu-id="555d4-111">Örnek 1: kaynak grubundan Web uygulaması alma</span><span class="sxs-lookup"><span data-stu-id="555d4-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="555d4-112">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan ContosoSite adlı Web uygulamasını alır.</span><span class="sxs-lookup"><span data-stu-id="555d4-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="555d4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="555d4-113">PARAMETERS</span></span>

### <span data-ttu-id="555d4-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="555d4-114">-AppServicePlan</span></span>
<span data-ttu-id="555d4-115">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="555d4-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="555d4-116">-DefaultProfile</span></span>
<span data-ttu-id="555d4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="555d4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="555d4-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="555d4-118">-Location</span></span>
<span data-ttu-id="555d4-119">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="555d4-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555d4-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="555d4-120">-Name</span></span>
<span data-ttu-id="555d4-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="555d4-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="555d4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="555d4-122">-ResourceGroupName</span></span>
<span data-ttu-id="555d4-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="555d4-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="555d4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="555d4-124">CommonParameters</span></span>
<span data-ttu-id="555d4-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="555d4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="555d4-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="555d4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="555d4-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="555d4-127">INPUTS</span></span>

### <span data-ttu-id="555d4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="555d4-128">System.String</span></span>

## <span data-ttu-id="555d4-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="555d4-129">OUTPUTS</span></span>

### <span data-ttu-id="555d4-130">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="555d4-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="555d4-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="555d4-131">NOTES</span></span>

## <span data-ttu-id="555d4-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="555d4-132">RELATED LINKS</span></span>

[<span data-ttu-id="555d4-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="555d4-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="555d4-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="555d4-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="555d4-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="555d4-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="555d4-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="555d4-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="555d4-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="555d4-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

