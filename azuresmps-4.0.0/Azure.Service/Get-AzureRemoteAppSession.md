---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106577"
---
# <span data-ttu-id="3e54b-101">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="3e54b-101">Get-AzureRemoteAppSession</span></span>

## <span data-ttu-id="3e54b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e54b-102">SYNOPSIS</span></span>
<span data-ttu-id="3e54b-103">Koleksiyon için tüm etkin ve bağlantı kesilen Azure RemoteApp oturumlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="3e54b-103">Lists all active and disconnected Azure RemoteApp sessions for a collection.</span></span>

## <span data-ttu-id="3e54b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e54b-104">SYNTAX</span></span>

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e54b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e54b-105">DESCRIPTION</span></span>
<span data-ttu-id="3e54b-106">**Get-AzureRemoteAppSession** cmdlet 'ı bir Azure RemoteApp koleksiyonu için tüm etkin ve bağlantısız Azure RemoteApp oturumlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="3e54b-106">The **Get-AzureRemoteAppSession** cmdlet lists all active and disconnected Azure RemoteApp sessions for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3e54b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e54b-107">EXAMPLES</span></span>

### <span data-ttu-id="3e54b-108">Örnek 1: koleksiyondaki tüm oturumları listeleme</span><span class="sxs-lookup"><span data-stu-id="3e54b-108">Example 1: List all the sessions in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

<span data-ttu-id="3e54b-109">Bu komut, ContosoApps adlı Azure RemoteApp koleksiyonundaki tüm oturumları listeler.</span><span class="sxs-lookup"><span data-stu-id="3e54b-109">This command lists all sessions in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="3e54b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e54b-110">PARAMETERS</span></span>

### <span data-ttu-id="3e54b-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="3e54b-111">-CollectionName</span></span>
<span data-ttu-id="3e54b-112">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e54b-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="3e54b-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="3e54b-113">-Profile</span></span>
<span data-ttu-id="3e54b-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e54b-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3e54b-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3e54b-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3e54b-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="3e54b-116">-UserUpn</span></span>
<span data-ttu-id="3e54b-117">Azure RemoteApp oturumlarının alınacağı bir kullanıcının Kullanıcı asıl adını (UPN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e54b-117">Specifies the user Principal Name (UPN) of a user for which to get Azure RemoteApp sessions.</span></span>
<span data-ttu-id="3e54b-118">Örneğin, UPN aşağıdaki biçimde olabilir: PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="3e54b-118">For example, the UPN can be in the following format: PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="3e54b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e54b-119">CommonParameters</span></span>
<span data-ttu-id="3e54b-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e54b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e54b-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e54b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e54b-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e54b-122">INPUTS</span></span>

## <span data-ttu-id="3e54b-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e54b-123">OUTPUTS</span></span>

## <span data-ttu-id="3e54b-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e54b-124">NOTES</span></span>

## <span data-ttu-id="3e54b-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e54b-125">RELATED LINKS</span></span>

[<span data-ttu-id="3e54b-126">Bağlantısı kesiliyor-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="3e54b-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="3e54b-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="3e54b-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="3e54b-128">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="3e54b-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


