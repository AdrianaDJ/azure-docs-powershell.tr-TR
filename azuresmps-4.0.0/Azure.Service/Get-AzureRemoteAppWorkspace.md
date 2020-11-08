---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 035B294E-6A1B-41E9-ACFF-D66F9C1A0B11
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9218862bb1e61abe548a94ed5297a6ce69237d54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105619"
---
# <span data-ttu-id="24adf-101">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="24adf-101">Get-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="24adf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24adf-102">SYNOPSIS</span></span>
<span data-ttu-id="24adf-103">Azure RemoteApp çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="24adf-103">Retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="24adf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24adf-104">SYNTAX</span></span>

```
Get-AzureRemoteAppWorkspace [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="24adf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24adf-105">DESCRIPTION</span></span>
<span data-ttu-id="24adf-106">**Get-AzureRemoteAppWorkspace** cmdlet 'ı Azure RemoteApp çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="24adf-106">The **Get-AzureRemoteAppWorkspace** cmdlet retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="24adf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24adf-107">EXAMPLES</span></span>

### <span data-ttu-id="24adf-108">Örnek 1: çalışma alanı hakkındaki bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="24adf-108">Example 1: Retrieve information about a workspace</span></span>
```
PS C:\> Get-AzureRemoteAppWorkspace
ClientUrl                               EndUserFeedName
---------                               ---------------
https://www.remoteapp.windowsazure.com/ Contoso Work Applications
```

<span data-ttu-id="24adf-109">Bu komut, Azure RemoteApp çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="24adf-109">This command retrieves information about the Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="24adf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24adf-110">PARAMETERS</span></span>

### <span data-ttu-id="24adf-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="24adf-111">-Profile</span></span>
<span data-ttu-id="24adf-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="24adf-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="24adf-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="24adf-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="24adf-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24adf-114">CommonParameters</span></span>
<span data-ttu-id="24adf-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24adf-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24adf-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24adf-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24adf-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24adf-117">INPUTS</span></span>

## <span data-ttu-id="24adf-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24adf-118">OUTPUTS</span></span>

## <span data-ttu-id="24adf-119">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24adf-119">NOTES</span></span>

## <span data-ttu-id="24adf-120">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24adf-120">RELATED LINKS</span></span>

[<span data-ttu-id="24adf-121">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="24adf-121">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)


