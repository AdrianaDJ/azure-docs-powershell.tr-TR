---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106322"
---
# <span data-ttu-id="7238c-101">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="7238c-101">Get-AzureRemoteAppOperationResult</span></span>

## <span data-ttu-id="7238c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7238c-102">SYNOPSIS</span></span>
<span data-ttu-id="7238c-103">Azure RemoteApp işleminin sonucunu getirir.</span><span class="sxs-lookup"><span data-stu-id="7238c-103">Retrieves the result of an Azure RemoteApp operation.</span></span>

## <span data-ttu-id="7238c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7238c-104">SYNTAX</span></span>

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7238c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7238c-105">DESCRIPTION</span></span>
<span data-ttu-id="7238c-106">**Get-AzureRemoteAppOperationResult** cmdlet 'i uzun süren bir Azure RemoteApp işlemi sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="7238c-106">The **Get-AzureRemoteAppOperationResult** cmdlet retrieves the result of a long-running Azure RemoteApp operation.</span></span>
<span data-ttu-id="7238c-107">Azure RemoteApp, hizmetin işlenmesi gereken birçok eylem için uzun süreli işlemler kullanır ve hemen geri dönemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="7238c-107">Azure RemoteApp uses long-running operations for many actions that require processing by the service and cannot return immediately.</span></span>
<span data-ttu-id="7238c-108">İzleme kimliklerini döndüren cmdlet **örnekleri,** **Update-AzureRemoteAppCollection** , **set-azureremoteapp**</span><span class="sxs-lookup"><span data-stu-id="7238c-108">Examples of cmdlets that return tracking IDs include **Update-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** , and others.</span></span>

## <span data-ttu-id="7238c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7238c-109">EXAMPLES</span></span>

### <span data-ttu-id="7238c-110">Örnek 1: işlem sonucu almak için izleme KIMLIĞI kullanma</span><span class="sxs-lookup"><span data-stu-id="7238c-110">Example 1: Use a tracking ID to get an operation result</span></span>
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

<span data-ttu-id="7238c-111">Bu komut, bir Azure RemoteApp işleminden döndürülen izleme KIMLIĞINI kaydeder.</span><span class="sxs-lookup"><span data-stu-id="7238c-111">This command saves the tracking ID returned from an Azure RemoteApp operation.</span></span>
<span data-ttu-id="7238c-112">İzleme KIMLIĞI, aşağıdaki komutta, **Get-Azureremoteappoperation'** a geçirilir.</span><span class="sxs-lookup"><span data-stu-id="7238c-112">The tracking ID is passed to **Get-AzureRemoteAppOperationResult** in the command that follows.</span></span>

## <span data-ttu-id="7238c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7238c-113">PARAMETERS</span></span>

### <span data-ttu-id="7238c-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="7238c-114">-Profile</span></span>
<span data-ttu-id="7238c-115">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7238c-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7238c-116">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7238c-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7238c-117">-Trackingıd</span><span class="sxs-lookup"><span data-stu-id="7238c-117">-TrackingId</span></span>
<span data-ttu-id="7238c-118">İşlemin izleme KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7238c-118">Specifies the tracking ID of an operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7238c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7238c-119">CommonParameters</span></span>
<span data-ttu-id="7238c-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7238c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7238c-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7238c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7238c-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7238c-122">INPUTS</span></span>

## <span data-ttu-id="7238c-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7238c-123">OUTPUTS</span></span>

## <span data-ttu-id="7238c-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7238c-124">NOTES</span></span>

## <span data-ttu-id="7238c-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7238c-125">RELATED LINKS</span></span>

[<span data-ttu-id="7238c-126">Bağlantısı kesiliyor-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="7238c-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="7238c-127">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="7238c-127">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)

[<span data-ttu-id="7238c-128">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="7238c-128">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


