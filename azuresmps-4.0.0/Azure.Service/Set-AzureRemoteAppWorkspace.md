---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106051"
---
# <span data-ttu-id="8d5f0-101">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="8d5f0-101">Set-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="8d5f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d5f0-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5f0-103">Azure RemoteApp çalışma alanının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8d5f0-103">Sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="8d5f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d5f0-104">SYNTAX</span></span>

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8d5f0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d5f0-105">DESCRIPTION</span></span>
<span data-ttu-id="8d5f0-106">**Set-AzureRemoteAppWorkspace** cmdlet 'ı bir Azure RemoteApp çalışma alanının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8d5f0-106">The **Set-AzureRemoteAppWorkspace** cmdlet sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="8d5f0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d5f0-107">EXAMPLES</span></span>

### <span data-ttu-id="8d5f0-108">Örnek 1: çalışma alanı adını ayarlama</span><span class="sxs-lookup"><span data-stu-id="8d5f0-108">Example 1: Set the workspace name</span></span>
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

<span data-ttu-id="8d5f0-109">Bu komut Azure RemoteApp çalışma alanı adını contoso Iş uygulamaları olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8d5f0-109">This command sets the Azure RemoteApp workspace name to Contoso Work Applications.</span></span>

## <span data-ttu-id="8d5f0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d5f0-110">PARAMETERS</span></span>

### <span data-ttu-id="8d5f0-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="8d5f0-111">-Profile</span></span>
<span data-ttu-id="8d5f0-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d5f0-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8d5f0-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8d5f0-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8d5f0-114">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="8d5f0-114">-WorkspaceName</span></span>
<span data-ttu-id="8d5f0-115">Azure RemoteApp çalışma alanı 'nın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d5f0-115">Specifies the name of the Azure RemoteApp workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5f0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5f0-116">CommonParameters</span></span>
<span data-ttu-id="8d5f0-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d5f0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5f0-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d5f0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5f0-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d5f0-119">INPUTS</span></span>

## <span data-ttu-id="8d5f0-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d5f0-120">OUTPUTS</span></span>

## <span data-ttu-id="8d5f0-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d5f0-121">NOTES</span></span>
* <span data-ttu-id="8d5f0-122">Belirli bir aboneliğin tüm Azure RemoteApp koleksiyonları paylaşılan bir çalışma alanında var.</span><span class="sxs-lookup"><span data-stu-id="8d5f0-122">All Azure RemoteApp collections for a specified subscription exist within a shared workspace.</span></span>

## <span data-ttu-id="8d5f0-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d5f0-123">RELATED LINKS</span></span>

[<span data-ttu-id="8d5f0-124">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="8d5f0-124">Get-AzureRemoteAppWorkspace</span></span>](./Get-AzureRemoteAppWorkspace.md)


