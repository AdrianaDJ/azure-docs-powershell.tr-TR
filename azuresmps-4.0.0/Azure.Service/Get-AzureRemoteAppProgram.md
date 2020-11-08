---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 636280D6-32C3-48EF-A271-A4E032F8B334
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0dab3720a4680805e16f695a1ab1b2350554e8f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106319"
---
# <span data-ttu-id="ca086-101">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="ca086-101">Get-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="ca086-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca086-102">SYNOPSIS</span></span>
<span data-ttu-id="ca086-103">Bir koleksiyon için yayımlanmış bir veya birden çok Azure RemoteApp programının özelliklerini getirir.</span><span class="sxs-lookup"><span data-stu-id="ca086-103">Retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="ca086-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca086-104">SYNTAX</span></span>

### <span data-ttu-id="ca086-105">FilterByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ca086-105">FilterByName (Default)</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-RemoteAppProgram] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca086-106">Filterbıyalıas</span><span class="sxs-lookup"><span data-stu-id="ca086-106">FilterByAlias</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca086-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca086-107">DESCRIPTION</span></span>
<span data-ttu-id="ca086-108">**Get-AzureRemoteAppProgram** cmdlet 'i, bir koleksiyon için yayımlanmış bir veya birden çok Azure RemoteApp programının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ca086-108">The **Get-AzureRemoteAppProgram** cmdlet retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="ca086-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca086-109">EXAMPLES</span></span>

### <span data-ttu-id="ca086-110">Örnek 1: bir programın özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="ca086-110">Example 1: Retrieve the properties of a program</span></span>
```
PS C:\> Get-AzureRemoteAppProgram -CollectionName "ContosoApps" -RemoteAppProgram "Finance App"

Alias                : edc85816-4b9e-4284-b3dc-faedb505f5d9

AvailableToUsers     : True

CommandLineArguments : 

IconPngUris          : Microsoft.Azure.Management.RemoteApp.Models.IconPngUrisType

IconUri              : https://liverdcxstorage.blob.core.windows.net/icons/12345678-1234-1234-1234-123412341234.ico?se=2015-03-01T17%3A29%3A51Z&amp;amp;sr=b&amp;amp;sp=r&amp;amp;sig=abcdCCavbcF%2asY4RascaBauishCasd2FasdBHtasd2BPasdi5dasdD

Name                 : Contoso Finance

Status               : Published

VirtualPath          : %SYSTEMDRIVE%\Program Files (x86)\Contoso Finance\Finance.exe
```

<span data-ttu-id="ca086-111">Bu komut, bir Azure RemoteApp programının özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="ca086-111">This command displays the properties of an Azure RemoteApp program.</span></span>
<span data-ttu-id="ca086-112">Finans uygulaması adlı program, ContosoApps adlı Azure RemoteApp koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="ca086-112">The program, named Finance App, is in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="ca086-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca086-113">PARAMETERS</span></span>

### <span data-ttu-id="ca086-114">-Diğer ad</span><span class="sxs-lookup"><span data-stu-id="ca086-114">-Alias</span></span>
<span data-ttu-id="ca086-115">Özelliklerin alınacağı programın diğer adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca086-115">Specifies the alias of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByAlias
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca086-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="ca086-116">-CollectionName</span></span>
<span data-ttu-id="ca086-117">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca086-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="ca086-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="ca086-118">-Profile</span></span>
<span data-ttu-id="ca086-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca086-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ca086-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ca086-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ca086-121">-RemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="ca086-121">-RemoteAppProgram</span></span>
<span data-ttu-id="ca086-122">Özelliklerini alacak olan programın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca086-122">Specifies the name of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ca086-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca086-123">CommonParameters</span></span>
<span data-ttu-id="ca086-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca086-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca086-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca086-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca086-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca086-126">INPUTS</span></span>

## <span data-ttu-id="ca086-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca086-127">OUTPUTS</span></span>

## <span data-ttu-id="ca086-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca086-128">NOTES</span></span>

## <span data-ttu-id="ca086-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca086-129">RELATED LINKS</span></span>

[<span data-ttu-id="ca086-130">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="ca086-130">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)

[<span data-ttu-id="ca086-131">Yayımdan kaldırma-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="ca086-131">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


