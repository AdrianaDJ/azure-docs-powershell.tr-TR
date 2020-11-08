---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106508"
---
# <span data-ttu-id="f39d7-101">Get-WAPackCloudVMRoleSizeProfile</span><span class="sxs-lookup"><span data-stu-id="f39d7-101">Get-WAPackCloudVMRoleSizeProfile</span></span>

## <span data-ttu-id="f39d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f39d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f39d7-103">Bulut VM rolü boyut profili nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="f39d7-103">Gets Cloud VM Role Size profile objects.</span></span>

## <span data-ttu-id="f39d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f39d7-104">SYNTAX</span></span>

### <span data-ttu-id="f39d7-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f39d7-105">Empty (Default)</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f39d7-106">FromName</span><span class="sxs-lookup"><span data-stu-id="f39d7-106">FromName</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f39d7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f39d7-107">DESCRIPTION</span></span>
<span data-ttu-id="f39d7-108">**Get-Wapackmrdvmrolesizeprofile** cmdlet 'i sanal MAKINELERIN bulut VM rolü boyut profili nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="f39d7-108">The **Get-WAPackCloudVMRoleSizeProfile** cmdlet gets Cloud VM Role size profile objects for virtual machines.</span></span>

## <span data-ttu-id="f39d7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f39d7-109">EXAMPLES</span></span>

### <span data-ttu-id="f39d7-110">Örnek 1: ad kullanarak bulut VM rolü boyut profili alma</span><span class="sxs-lookup"><span data-stu-id="f39d7-110">Example 1: Get a Cloud VM Role size profile by using a name</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

<span data-ttu-id="f39d7-111">Bu komut, küçük olan boyut profilini alır.</span><span class="sxs-lookup"><span data-stu-id="f39d7-111">This command gets the size profile named Small.</span></span>

### <span data-ttu-id="f39d7-112">Örnek 2: tüm bulut VM rolü</span><span class="sxs-lookup"><span data-stu-id="f39d7-112">Example 2: Get all Cloud VM Role size profiles</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

<span data-ttu-id="f39d7-113">Bu komut, tüm boyut profillerini alır.</span><span class="sxs-lookup"><span data-stu-id="f39d7-113">This command gets all the size profiles.</span></span>

## <span data-ttu-id="f39d7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f39d7-114">PARAMETERS</span></span>

### <span data-ttu-id="f39d7-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f39d7-115">-Name</span></span>
<span data-ttu-id="f39d7-116">Bulut VM rol boyutu profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f39d7-116">Specifies the name of a Cloud VM Role size profile.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f39d7-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="f39d7-117">-Profile</span></span>
<span data-ttu-id="f39d7-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f39d7-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f39d7-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f39d7-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f39d7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39d7-120">CommonParameters</span></span>
<span data-ttu-id="f39d7-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f39d7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39d7-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f39d7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39d7-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f39d7-123">INPUTS</span></span>

## <span data-ttu-id="f39d7-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f39d7-124">OUTPUTS</span></span>

## <span data-ttu-id="f39d7-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f39d7-125">NOTES</span></span>

## <span data-ttu-id="f39d7-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f39d7-126">RELATED LINKS</span></span>

[<span data-ttu-id="f39d7-127">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f39d7-127">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


