---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: FCDEA955-EB64-4EEA-9F4A-04E2C1F0A831
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83664e8be9241782e42d7ba7634691668ed575f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106315"
---
# <span data-ttu-id="3f4dd-101">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="3f4dd-101">Get-AzureRemoteAppStartMenuProgram</span></span>

## <span data-ttu-id="3f4dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4dd-103">Azure RemoteApp koleksiyonundaki Başlat menüsü programlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="3f4dd-103">Lists the Start Menu programs in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3f4dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f4dd-104">SYNTAX</span></span>

```
Get-AzureRemoteAppStartMenuProgram [-CollectionName] <String> [[-ProgramName] <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3f4dd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f4dd-105">DESCRIPTION</span></span>
<span data-ttu-id="3f4dd-106">**Get-AzureRemoteAppStartMenuProgram** cmdlet 'i, şablon görüntüsünde Azure RemoteApp koleksiyonunun kullandığı Başlat menüsü programlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="3f4dd-106">The **Get-AzureRemoteAppStartMenuProgram** cmdlet lists the Start Menu programs in the template image that an Azure RemoteApp collection uses.</span></span>

## <span data-ttu-id="3f4dd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f4dd-107">EXAMPLES</span></span>

### <span data-ttu-id="3f4dd-108">Örnek 1: koleksiyon için başlangıç menüsü programlarını listeleme</span><span class="sxs-lookup"><span data-stu-id="3f4dd-108">Example 1: List the Start Menu programs for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppStartMenuProgram -CollectionName "ContosoApps"
```

<span data-ttu-id="3f4dd-109">Bu komut, ContosoApps koleksiyonunun Başlat menüsü programlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3f4dd-109">This command returns the list of Start Menu programs for the ContosoApps collection.</span></span>

## <span data-ttu-id="3f4dd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f4dd-110">PARAMETERS</span></span>

### <span data-ttu-id="3f4dd-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="3f4dd-111">-CollectionName</span></span>
<span data-ttu-id="3f4dd-112">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f4dd-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4dd-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="3f4dd-113">-Profile</span></span>
<span data-ttu-id="3f4dd-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f4dd-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3f4dd-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3f4dd-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4dd-116">-ProgramName</span><span class="sxs-lookup"><span data-stu-id="3f4dd-116">-ProgramName</span></span>
<span data-ttu-id="3f4dd-117">Listesi oluşturulacak programın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f4dd-117">Specifies the name of a program for which to list information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="3f4dd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4dd-118">CommonParameters</span></span>
<span data-ttu-id="3f4dd-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f4dd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4dd-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f4dd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4dd-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f4dd-121">INPUTS</span></span>

## <span data-ttu-id="3f4dd-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f4dd-122">OUTPUTS</span></span>

## <span data-ttu-id="3f4dd-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f4dd-123">NOTES</span></span>

## <span data-ttu-id="3f4dd-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f4dd-124">RELATED LINKS</span></span>

[<span data-ttu-id="3f4dd-125">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3f4dd-125">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)


