---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 000B2335-E374-47CC-8165-40AE807C090F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c097884326d1430804f1d577629b62041bfd402b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106146"
---
# <span data-ttu-id="ca262-101">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="ca262-101">Remove-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="ca262-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca262-102">SYNOPSIS</span></span>
<span data-ttu-id="ca262-103">Azure RemoteApp sanal ağını siler.</span><span class="sxs-lookup"><span data-stu-id="ca262-103">Deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="ca262-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca262-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppVNet -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ca262-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca262-105">DESCRIPTION</span></span>
<span data-ttu-id="ca262-106">**Remove-AzureRemoteAppVNet** cmdlet 'ı bir Azure RemoteApp sanal ağını siler.</span><span class="sxs-lookup"><span data-stu-id="ca262-106">The **Remove-AzureRemoteAppVNet** cmdlet deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="ca262-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca262-107">EXAMPLES</span></span>

### <span data-ttu-id="ca262-108">Örnek 1: belirtilen sanal ağı silme</span><span class="sxs-lookup"><span data-stu-id="ca262-108">Example 1: Delete a specified virtual network</span></span>
```
PS C:\> Remove-AzureRemoteAppVnet -VNetName "ContosoVNet"
```

<span data-ttu-id="ca262-109">Bu komut, ContosoVNet adlı sanal ağı siler.</span><span class="sxs-lookup"><span data-stu-id="ca262-109">This command deletes the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="ca262-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca262-110">PARAMETERS</span></span>

### <span data-ttu-id="ca262-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="ca262-111">-Profile</span></span>
<span data-ttu-id="ca262-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca262-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ca262-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ca262-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ca262-114">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="ca262-114">-VNetName</span></span>
<span data-ttu-id="ca262-115">Silinecek Azure RemoteApp sanal ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca262-115">Specifies the name of the Azure RemoteApp virtual network to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca262-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca262-116">CommonParameters</span></span>
<span data-ttu-id="ca262-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca262-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca262-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca262-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca262-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca262-119">INPUTS</span></span>

## <span data-ttu-id="ca262-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca262-120">OUTPUTS</span></span>

## <span data-ttu-id="ca262-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca262-121">NOTES</span></span>

## <span data-ttu-id="ca262-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca262-122">RELATED LINKS</span></span>

[<span data-ttu-id="ca262-123">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="ca262-123">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="ca262-124">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="ca262-124">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


