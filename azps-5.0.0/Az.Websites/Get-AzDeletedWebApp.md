---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279930"
---
# <span data-ttu-id="145fe-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="145fe-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="145fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="145fe-102">SYNOPSIS</span></span>
<span data-ttu-id="145fe-103">Aboneliğin silinen Web uygulamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="145fe-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="145fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="145fe-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="145fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="145fe-105">DESCRIPTION</span></span>
<span data-ttu-id="145fe-106">**Get-AzDeletedWebApp** cmdlet 'i, abonelikteki tüm silinen Web uygulamalarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="145fe-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="145fe-107">Silinen uygulamalar, isteğe bağlı olarak kaynak grubu, ad ve yuvaya göre filtrelenebilir.</span><span class="sxs-lookup"><span data-stu-id="145fe-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="145fe-108">Aynı ada ve kaynak grubuna sahip birden fazla silinen uygulama olabilir.</span><span class="sxs-lookup"><span data-stu-id="145fe-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="145fe-109">Aynı adı paylaşan silinen uygulamaları ayırt etmek için DeletionTime 'i denetleyin.</span><span class="sxs-lookup"><span data-stu-id="145fe-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="145fe-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="145fe-110">EXAMPLES</span></span>

### <span data-ttu-id="145fe-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="145fe-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="145fe-112">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan ContosoSite adlı silinmiş uygulamaları alır.</span><span class="sxs-lookup"><span data-stu-id="145fe-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="145fe-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="145fe-113">PARAMETERS</span></span>

### <span data-ttu-id="145fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="145fe-114">-DefaultProfile</span></span>
<span data-ttu-id="145fe-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="145fe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="145fe-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="145fe-116">-Location</span></span>
<span data-ttu-id="145fe-117">Silinen uygulamanın konumu.</span><span class="sxs-lookup"><span data-stu-id="145fe-117">The location of the deleted app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145fe-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="145fe-118">-Name</span></span>
<span data-ttu-id="145fe-119">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="145fe-119">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145fe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="145fe-120">-ResourceGroupName</span></span>
<span data-ttu-id="145fe-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="145fe-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145fe-122">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="145fe-122">-Slot</span></span>
<span data-ttu-id="145fe-123">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="145fe-123">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="145fe-124">CommonParameters</span></span>
<span data-ttu-id="145fe-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="145fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="145fe-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="145fe-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="145fe-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="145fe-127">INPUTS</span></span>

### <span data-ttu-id="145fe-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="145fe-128">None</span></span>

## <span data-ttu-id="145fe-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="145fe-129">OUTPUTS</span></span>

### <span data-ttu-id="145fe-130">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="145fe-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="145fe-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="145fe-131">NOTES</span></span>

## <span data-ttu-id="145fe-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="145fe-132">RELATED LINKS</span></span>

[<span data-ttu-id="145fe-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="145fe-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)