---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106477"
---
# <span data-ttu-id="b2a4b-101">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="b2a4b-101">Remove-AzureEnvironment</span></span>

## <span data-ttu-id="b2a4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="b2a4b-103">Windows PowerShell 'den bir Azure ortamını siler.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-103">Deletes an Azure environment from Windows PowerShell.</span></span>

## <span data-ttu-id="b2a4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2a4b-104">SYNTAX</span></span>

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b2a4b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2a4b-105">DESCRIPTION</span></span>
<span data-ttu-id="b2a4b-106">**Remove-AzureEnvironment** cmdlet 'i, gezici profilinizden bir Azure ortamı siler, böylece Windows PowerShell bunu bulamaz.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-106">The **Remove-AzureEnvironment** cmdlet deletes an Azure environment from your roaming profile so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="b2a4b-107">Bu cmdlet, Microsoft Azure 'dan ortamı silmez veya gerçek ortamı hiçbir şekilde değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-107">This cmdlet does not delete the environment from Microsoft Azure, or change the actual environment in any way.</span></span>

<span data-ttu-id="b2a4b-108">Bir Azure ortamında, Çin 'de 21Vianet tarafından sağlanan, genel Azure ve Azure için AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-108">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="b2a4b-109">Ayrıca, Azure paketini ve WAPack cmdlet 'lerini kullanarak şirket içi Azure ortamları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-109">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="b2a4b-110">Daha fazla bilgi için bkz: [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b2a4b-110">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

## <span data-ttu-id="b2a4b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2a4b-111">EXAMPLES</span></span>

### <span data-ttu-id="b2a4b-112">Örnek 1: bir ortamı silme</span><span class="sxs-lookup"><span data-stu-id="b2a4b-112">Example 1: Delete an environment</span></span>
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

<span data-ttu-id="b2a4b-113">Bu komut, Windows PowerShell 'den ContosoEnv ortamını siler.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-113">This command deletes the ContosoEnv environment from Windows PowerShell.</span></span>

### <span data-ttu-id="b2a4b-114">Örnek 2: birden çok ortamı silme</span><span class="sxs-lookup"><span data-stu-id="b2a4b-114">Example 2: Delete multiple environments</span></span>
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

<span data-ttu-id="b2a4b-115">Bu komut, adları Windows PowerShell 'den "contoso" ile başlayan ortamları siler.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-115">This command deletes environments whose names begin with "Contoso" from Windows PowerShell.</span></span>

## <span data-ttu-id="b2a4b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2a4b-116">PARAMETERS</span></span>

### <span data-ttu-id="b2a4b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b2a4b-117">-Force</span></span>
<span data-ttu-id="b2a4b-118">Onay istemini bastırır.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-118">Suppresses the confirmation prompt.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2a4b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b2a4b-119">-Name</span></span>
<span data-ttu-id="b2a4b-120">Kaldırılacak ortamın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-120">Specifies the name of the environment to remove.</span></span>
<span data-ttu-id="b2a4b-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-121">This parameter is required.</span></span>
<span data-ttu-id="b2a4b-122">Bu parametre değeri büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-122">This parameter value is case-sensitive.</span></span>
<span data-ttu-id="b2a4b-123">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-123">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2a4b-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="b2a4b-124">-Profile</span></span>
<span data-ttu-id="b2a4b-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b2a4b-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b2a4b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a4b-127">CommonParameters</span></span>
<span data-ttu-id="b2a4b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a4b-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2a4b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a4b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2a4b-130">INPUTS</span></span>

### <span data-ttu-id="b2a4b-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b2a4b-131">None</span></span>
<span data-ttu-id="b2a4b-132">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-132">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="b2a4b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2a4b-133">OUTPUTS</span></span>

### <span data-ttu-id="b2a4b-134">None veya System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2a4b-134">None or System.Boolean</span></span>
<span data-ttu-id="b2a4b-135">*Passin* parametresini kullanıyorsanız, bu cmdlet bir Boole değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-135">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="b2a4b-136">Aksi takdirde hiçbir çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="b2a4b-136">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="b2a4b-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2a4b-137">NOTES</span></span>

## <span data-ttu-id="b2a4b-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2a4b-138">RELATED LINKS</span></span>

[<span data-ttu-id="b2a4b-139">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="b2a4b-139">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="b2a4b-140">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="b2a4b-140">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="b2a4b-141">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="b2a4b-141">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


