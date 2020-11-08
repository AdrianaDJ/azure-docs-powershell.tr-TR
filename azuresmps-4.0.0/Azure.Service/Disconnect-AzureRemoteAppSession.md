---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 514C33F8-F0B8-4F37-AB2D-BB54DD754931
online version: ''
schema: 2.0.0
ms.openlocfilehash: c256ce8ba720eb08ffec2ab56ecca40ab74f4948
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105686"
---
# <span data-ttu-id="205fe-101">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="205fe-101">Disconnect-AzureRemoteAppSession</span></span>

## <span data-ttu-id="205fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="205fe-102">SYNOPSIS</span></span>
<span data-ttu-id="205fe-103">Azure RemoteApp oturumunun bağlantısını keser.</span><span class="sxs-lookup"><span data-stu-id="205fe-103">Disconnects an Azure RemoteApp session.</span></span>

## <span data-ttu-id="205fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="205fe-104">SYNTAX</span></span>

```
Disconnect-AzureRemoteAppSession [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="205fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="205fe-105">DESCRIPTION</span></span>
<span data-ttu-id="205fe-106">**Bağlantı kesilmesi-AzureRemoteAppSession** cmdlet 'ı kullanıcının Azure RemoteApp oturumunun bağlantısını keser.</span><span class="sxs-lookup"><span data-stu-id="205fe-106">The **Disconnect-AzureRemoteAppSession** cmdlet disconnects a user's Azure RemoteApp session.</span></span>
<span data-ttu-id="205fe-107">Kullanıcının istemcisi Azure RemoteApp oturumuyla bağlantıyı keser, ancak kullanıcının programları çalışmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="205fe-107">The user's client disconnects from their Azure RemoteApp session, but the user's programs continue to run.</span></span>

## <span data-ttu-id="205fe-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="205fe-108">EXAMPLES</span></span>

### <span data-ttu-id="205fe-109">Örnek 1: kullanıcının oturumunun bağlantısının kesilmesi</span><span class="sxs-lookup"><span data-stu-id="205fe-109">Example 1: Disconnect a user's session</span></span>
```
PS C:\> Disconnect-AzureRemoteAppSession -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="205fe-110">Bu komut, UPN 'si olan kullanıcının ContosoApps koleksiyonundaki Azure RemoteApp oturumunun bağlantısını keser PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="205fe-110">This command disconnects the Azure RemoteApp session in the ContosoApps collection for the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="205fe-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="205fe-111">PARAMETERS</span></span>

### <span data-ttu-id="205fe-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="205fe-112">-CollectionName</span></span>
<span data-ttu-id="205fe-113">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="205fe-113">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="205fe-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="205fe-114">-Profile</span></span>
<span data-ttu-id="205fe-115">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="205fe-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="205fe-116">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="205fe-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="205fe-117">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="205fe-117">-UserUpn</span></span>
<span data-ttu-id="205fe-118">Bir kullanıcının Kullanıcı asıl adını (UPN) belirtir PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="205fe-118">Specifies the User Principal Name (UPN) of a user, for example PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205fe-119">CommonParameters</span></span>
<span data-ttu-id="205fe-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="205fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205fe-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="205fe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205fe-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="205fe-122">INPUTS</span></span>

## <span data-ttu-id="205fe-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="205fe-123">OUTPUTS</span></span>

## <span data-ttu-id="205fe-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="205fe-124">NOTES</span></span>

## <span data-ttu-id="205fe-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="205fe-125">RELATED LINKS</span></span>

[<span data-ttu-id="205fe-126">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="205fe-126">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="205fe-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="205fe-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="205fe-128">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="205fe-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


