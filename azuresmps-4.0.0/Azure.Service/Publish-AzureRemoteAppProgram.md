---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F101382E-B015-4913-B4A0-8827EC423319
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37c4bf3ad2c2aaf74f268b18d17b6af71f4f2fc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105884"
---
# <span data-ttu-id="8215a-101">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="8215a-101">Publish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="8215a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8215a-102">SYNOPSIS</span></span>
<span data-ttu-id="8215a-103">Bir Azure RemoteApp programı yayımlar.</span><span class="sxs-lookup"><span data-stu-id="8215a-103">Publishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="8215a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8215a-104">SYNTAX</span></span>

### <span data-ttu-id="8215a-105">Uygulama kimliği (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8215a-105">App Id (Default)</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-StartMenuAppId] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8215a-106">Uygulama yolu</span><span class="sxs-lookup"><span data-stu-id="8215a-106">App Path</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-FileVirtualPath] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8215a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8215a-107">DESCRIPTION</span></span>
<span data-ttu-id="8215a-108">**Publish-AzureRemoteAppProgram** cmdlet 'ı, Azure RemoteApp koleksiyonunun kullanıcılarına uygun kılan bir Azure RemoteApp programı yayımlar.</span><span class="sxs-lookup"><span data-stu-id="8215a-108">The **Publish-AzureRemoteAppProgram** cmdlet publishes an Azure RemoteApp program, which makes it available to users of the Azure RemoteApp collection.</span></span>

## <span data-ttu-id="8215a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8215a-109">EXAMPLES</span></span>

### <span data-ttu-id="8215a-110">Örnek 1: bir program derleme içinde Yayınlanın</span><span class="sxs-lookup"><span data-stu-id="8215a-110">Example 1: Publish a program in a collection</span></span>
```
PS C:\> Publish-AzureRemoteAppProgram -CollectionName "ContosoApps" -StartMenuAppId "a3732322-89a5-4cbc-9844-9634c74d337f" -DisplayName "Finance App"
```

<span data-ttu-id="8215a-111">Bu komut, programı Başlat menüsüne eklemek için belirtilen *Startmenuappıd* Ile contosoapps koleksiyonunda yayımlar.</span><span class="sxs-lookup"><span data-stu-id="8215a-111">This command publishes the program in the ContosoApps collection with the specified *StartMenuAppId* to add the program to the Start Menu.</span></span>
<span data-ttu-id="8215a-112">Yayınlanan uygulama "Finans uygulaması" görünen adına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="8215a-112">The published app will have a display name of "Finance App".</span></span>

## <span data-ttu-id="8215a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8215a-113">PARAMETERS</span></span>

### <span data-ttu-id="8215a-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="8215a-114">-CollectionName</span></span>
<span data-ttu-id="8215a-115">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8215a-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="8215a-116">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="8215a-116">-CommandLine</span></span>
<span data-ttu-id="8215a-117">Bu cmdlet 'in yayımladığı programın komut satırı bağımsız değişkenlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8215a-117">Specifies command-line arguments for the program that this cmdlet publishes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8215a-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8215a-118">-DisplayName</span></span>
<span data-ttu-id="8215a-119">Azure RemoteApp programının kullanımı kolay görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8215a-119">Specifies the user-friendly display name of the Azure RemoteApp program.</span></span>
<span data-ttu-id="8215a-120">Kullanıcılar bunu uygulamanın adı olarak görür.</span><span class="sxs-lookup"><span data-stu-id="8215a-120">Users see this as the name of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8215a-121">-FileVirtualPath</span><span class="sxs-lookup"><span data-stu-id="8215a-121">-FileVirtualPath</span></span>
<span data-ttu-id="8215a-122">Programın şablon görüntüsü içindeki programın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8215a-122">Specifies the path of the program within the template image of the program.</span></span>

```yaml
Type: String
Parameter Sets: App Path
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8215a-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="8215a-123">-Profile</span></span>
<span data-ttu-id="8215a-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8215a-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8215a-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8215a-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8215a-126">-Startmenuappıd</span><span class="sxs-lookup"><span data-stu-id="8215a-126">-StartMenuAppId</span></span>
<span data-ttu-id="8215a-127">Programı Başlat menüsüne eklemek için bu cmdlet 'in kullandığı GUID 'YI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8215a-127">Specifies a GUID that this cmdlet uses to add the program to the Start Menu.</span></span>

```yaml
Type: String
Parameter Sets: App Id
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8215a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8215a-128">CommonParameters</span></span>
<span data-ttu-id="8215a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8215a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8215a-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8215a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8215a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8215a-131">INPUTS</span></span>

## <span data-ttu-id="8215a-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8215a-132">OUTPUTS</span></span>

## <span data-ttu-id="8215a-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8215a-133">NOTES</span></span>

## <span data-ttu-id="8215a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8215a-134">RELATED LINKS</span></span>

[<span data-ttu-id="8215a-135">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="8215a-135">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="8215a-136">Yayımdan kaldırma-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="8215a-136">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


