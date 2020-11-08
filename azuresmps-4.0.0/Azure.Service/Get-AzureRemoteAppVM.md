---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D40937C2-9BF7-4371-A64C-B44F5B6B895E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c9882e805504b2e3b2e4f4ebbe661268b2327a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106571"
---
# <span data-ttu-id="17345-101">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="17345-101">Get-AzureRemoteAppVM</span></span>

## <span data-ttu-id="17345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17345-102">SYNOPSIS</span></span>
<span data-ttu-id="17345-103">Bir Azure RemoteApp koleksiyonundaki sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="17345-103">Gets the virtual machines in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="17345-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17345-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVM -CollectionName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="17345-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="17345-105">DESCRIPTION</span></span>
<span data-ttu-id="17345-106">**Get-AzureRemoteAppVM** cmdlet 'i oturum barındırma Için bir Azure RemoteApp koleksiyonu altında oluşturulmuş sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="17345-106">The **Get-AzureRemoteAppVM** cmdlet gets the virtual machines created under an Azure RemoteApp collection for session hosting.</span></span>

## <span data-ttu-id="17345-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17345-107">EXAMPLES</span></span>

### <span data-ttu-id="17345-108">Örnek 1: bir koleksiyonda sanal makineleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="17345-108">Example 1: Display the virtual machines in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppVM -CollectionName "Contoso"
```

<span data-ttu-id="17345-109">Bu komut, contoso adlı bir Azure RemoteApp koleksiyonunda oturum barındırma için kullanılan sanal makineleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="17345-109">This command displays the virtual machines used for session hosting in an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="17345-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17345-110">PARAMETERS</span></span>

### <span data-ttu-id="17345-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="17345-111">-CollectionName</span></span>
<span data-ttu-id="17345-112">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17345-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17345-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="17345-113">-Profile</span></span>
<span data-ttu-id="17345-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17345-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="17345-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="17345-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="17345-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17345-116">CommonParameters</span></span>
<span data-ttu-id="17345-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17345-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17345-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17345-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17345-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17345-119">INPUTS</span></span>

## <span data-ttu-id="17345-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17345-120">OUTPUTS</span></span>

## <span data-ttu-id="17345-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17345-121">NOTES</span></span>

## <span data-ttu-id="17345-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17345-122">RELATED LINKS</span></span>

[<span data-ttu-id="17345-123">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="17345-123">Restart-AzureRemoteAppVM</span></span>](./Restart-AzureRemoteAppVM.md)


