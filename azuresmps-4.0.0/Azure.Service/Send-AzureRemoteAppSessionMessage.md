---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 6236AD2C-D54D-4013-9977-AD1E6EAC2F21
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac0283f6c9de9a1cd5f17abd6e27ebb2c8629505
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106433"
---
# <span data-ttu-id="f5d83-101">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="f5d83-101">Send-AzureRemoteAppSessionMessage</span></span>

## <span data-ttu-id="f5d83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5d83-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d83-103">Kullanıcıya ileti gönderir.</span><span class="sxs-lookup"><span data-stu-id="f5d83-103">Sends a message to a user.</span></span>

## <span data-ttu-id="f5d83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5d83-104">SYNTAX</span></span>

```
Send-AzureRemoteAppSessionMessage [-CollectionName] <String> [-UserUpn] <String> [-Message] <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f5d83-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5d83-105">DESCRIPTION</span></span>
<span data-ttu-id="f5d83-106">**Send-AzureRemoteAppSessionMessage** cmdlet 'ı, Azure RemoteApp oturumuna bağlı bir kullanıcıya ileti gönderir.</span><span class="sxs-lookup"><span data-stu-id="f5d83-106">The **Send-AzureRemoteAppSessionMessage** cmdlet sends a message to a user who is connected to an Azure RemoteApp session.</span></span>

## <span data-ttu-id="f5d83-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5d83-107">EXAMPLES</span></span>

### <span data-ttu-id="f5d83-108">Örnek 1: kullanıcıya ileti gönderme</span><span class="sxs-lookup"><span data-stu-id="f5d83-108">Example 1: Send a message to a user</span></span>
```
PS C:\> Send-AzureRemoteAppSessionMessage -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com" -Message "The system will be going down for maintenance soon.  Please save your work and close your RemoteApps."
```

<span data-ttu-id="f5d83-109">Bu komut, UPN 'si olan kullanıcıya bir ileti gönderir PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="f5d83-109">This command sends a message to the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="f5d83-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5d83-110">PARAMETERS</span></span>

### <span data-ttu-id="f5d83-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="f5d83-111">-CollectionName</span></span>
<span data-ttu-id="f5d83-112">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5d83-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="f5d83-113">-İleti</span><span class="sxs-lookup"><span data-stu-id="f5d83-113">-Message</span></span>
<span data-ttu-id="f5d83-114">Gönderilecek iletiyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5d83-114">Specifies the message to send.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d83-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="f5d83-115">-Profile</span></span>
<span data-ttu-id="f5d83-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5d83-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f5d83-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f5d83-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5d83-118">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="f5d83-118">-UserUpn</span></span>
<span data-ttu-id="f5d83-119">Kullanıcının Kullanıcı asıl adını (UPN) belirtir; Örneğin PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="f5d83-119">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="f5d83-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d83-120">CommonParameters</span></span>
<span data-ttu-id="f5d83-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5d83-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d83-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5d83-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d83-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5d83-123">INPUTS</span></span>

## <span data-ttu-id="f5d83-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5d83-124">OUTPUTS</span></span>

## <span data-ttu-id="f5d83-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5d83-125">NOTES</span></span>

## <span data-ttu-id="f5d83-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5d83-126">RELATED LINKS</span></span>

[<span data-ttu-id="f5d83-127">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="f5d83-127">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="f5d83-128">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="f5d83-128">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="f5d83-129">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="f5d83-129">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


