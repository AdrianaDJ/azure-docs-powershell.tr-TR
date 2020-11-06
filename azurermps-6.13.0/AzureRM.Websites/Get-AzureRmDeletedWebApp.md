---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
ms.openlocfilehash: 75ad4e1fabb511ee4ca3cff024389a8e826aeadd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590791"
---
# <span data-ttu-id="89c8a-101">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="89c8a-101">Get-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="89c8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="89c8a-103">Aboneliğin silinen Web uygulamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="89c8a-103">Gets deleted web apps in the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89c8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89c8a-104">SYNTAX</span></span>

```
Get-AzureRmDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89c8a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="89c8a-105">DESCRIPTION</span></span>
<span data-ttu-id="89c8a-106">**Get-AzureRmDeletedWebApp** cmdlet 'i, abonelikteki tüm silinen Web uygulamalarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="89c8a-106">The **Get-AzureRmDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="89c8a-107">Silinen uygulamalar, isteğe bağlı olarak kaynak grubu, ad ve yuvaya göre filtrelenebilir.</span><span class="sxs-lookup"><span data-stu-id="89c8a-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="89c8a-108">Aynı ada ve kaynak grubuna sahip birden fazla silinen uygulama olabilir.</span><span class="sxs-lookup"><span data-stu-id="89c8a-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="89c8a-109">Aynı adı paylaşan silinen uygulamaları ayırt etmek için DeletionTime 'i denetleyin.</span><span class="sxs-lookup"><span data-stu-id="89c8a-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="89c8a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89c8a-110">EXAMPLES</span></span>

### <span data-ttu-id="89c8a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="89c8a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="89c8a-112">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan ContosoSite adlı silinmiş uygulamaları alır.</span><span class="sxs-lookup"><span data-stu-id="89c8a-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="89c8a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89c8a-113">PARAMETERS</span></span>

### <span data-ttu-id="89c8a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c8a-114">-DefaultProfile</span></span>
<span data-ttu-id="89c8a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89c8a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89c8a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="89c8a-116">-Name</span></span>
<span data-ttu-id="89c8a-117">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="89c8a-117">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c8a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89c8a-118">-ResourceGroupName</span></span>
<span data-ttu-id="89c8a-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="89c8a-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c8a-120">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="89c8a-120">-Slot</span></span>
<span data-ttu-id="89c8a-121">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="89c8a-121">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c8a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c8a-122">CommonParameters</span></span>
<span data-ttu-id="89c8a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89c8a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="89c8a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89c8a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c8a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89c8a-125">INPUTS</span></span>

### <span data-ttu-id="89c8a-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="89c8a-126">None</span></span>

## <span data-ttu-id="89c8a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89c8a-127">OUTPUTS</span></span>

### <span data-ttu-id="89c8a-128">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="89c8a-128">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="89c8a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89c8a-129">NOTES</span></span>

## <span data-ttu-id="89c8a-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89c8a-130">RELATED LINKS</span></span>

[<span data-ttu-id="89c8a-131">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="89c8a-131">Restore-AzureRmDeletedWebApp</span></span>](./Restore-AzureRmDeletedWebApp.md)
