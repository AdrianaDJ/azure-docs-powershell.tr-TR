---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F83D698B-DC48-4ACD-AD2E-4AAECBDA196B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc8081c9f81305b96b1ac227b9766352ce94b06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106084"
---
# <span data-ttu-id="67869-101">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="67869-101">Restart-AzureRemoteAppVM</span></span>

## <span data-ttu-id="67869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67869-102">SYNOPSIS</span></span>
<span data-ttu-id="67869-103">Azure RemoteApp koleksiyonunda sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="67869-103">Restarts a virtual machine in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="67869-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67869-104">SYNTAX</span></span>

```
Restart-AzureRemoteAppVM -CollectionName <String> -UserUpn <String> [-LogoffMessage <String>]
 [-LogoffWaitSeconds <Int32>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67869-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="67869-105">DESCRIPTION</span></span>
<span data-ttu-id="67869-106">**Restart-AzureRemoteAppVM** cmdlet 'i, belirtilen kullanıcının bağlı olduğu bir Azure RemoteApp koleksiyonundaki sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="67869-106">The **Restart-AzureRemoteAppVM** cmdlet restarts a virtual machine in an Azure RemoteApp collection on which the specified user is connected.</span></span>

## <span data-ttu-id="67869-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67869-107">EXAMPLES</span></span>

### <span data-ttu-id="67869-108">Örnek 1: sanal makineyi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="67869-108">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRemoteAppVM -CollectionName "ContosoVNet" -UserUPN "PattiFuller@contoso.com"
```

<span data-ttu-id="67869-109">Bu komut contoso adlı bir Azure RemoteApp koleksiyonundaki sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="67869-109">This command restarts a virtual machine in an Azure RemoteApp collection named Contoso.</span></span>
<span data-ttu-id="67869-110">Kullanıcı, PattiFuller@contoso.com Bu sanal makineyi içeren koleksiyona bağlanır.</span><span class="sxs-lookup"><span data-stu-id="67869-110">The user PattiFuller@contoso.com is connected to the collection which contains this virtual machine.</span></span>

## <span data-ttu-id="67869-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67869-111">PARAMETERS</span></span>

### <span data-ttu-id="67869-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="67869-112">-CollectionName</span></span>
<span data-ttu-id="67869-113">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67869-113">Specifies the name of an Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="67869-114">-LogoffMessage</span><span class="sxs-lookup"><span data-stu-id="67869-114">-LogoffMessage</span></span>
<span data-ttu-id="67869-115">Bu cmdlet oturumu kapatmadan önce sanal makineye bağlı kullanıcılar için gösterilen bir uyarı iletisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="67869-115">Specifies a warning message shown to users connected to the virtual machine before this cmdlet logs them off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67869-116">-LogoffWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="67869-116">-LogoffWaitSeconds</span></span>
<span data-ttu-id="67869-117">Bu cmdlet 'in kullanıcıları kapatmadan önce bekleyeceği süreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="67869-117">Specifies how long this cmdlet waits before it logs users off.</span></span>
<span data-ttu-id="67869-118">Varsayılan değer 60 saniyedir.</span><span class="sxs-lookup"><span data-stu-id="67869-118">The default value is 60 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67869-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="67869-119">-Profile</span></span>
<span data-ttu-id="67869-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67869-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67869-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="67869-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="67869-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="67869-122">-UserUpn</span></span>
<span data-ttu-id="67869-123">Bu cmdlet 'in sanal makineyi yeniden başlattığı kullanıcının Kullanıcı asıl adını (UPN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="67869-123">Specifies the user principal name (UPN) of the user for whom this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="67869-124">Koleksiyonda ve bağlı UPN 'lerle sanal makineleri edinmek için **Get-AzureRemoteAppVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="67869-124">To obtain virtual machines in the collection and connected UPNs, use the **Get-AzureRemoteAppVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67869-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="67869-125">-Confirm</span></span>
<span data-ttu-id="67869-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="67869-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67869-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67869-127">-WhatIf</span></span>
<span data-ttu-id="67869-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="67869-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67869-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="67869-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67869-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67869-130">CommonParameters</span></span>
<span data-ttu-id="67869-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67869-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67869-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67869-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67869-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67869-133">INPUTS</span></span>

## <span data-ttu-id="67869-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67869-134">OUTPUTS</span></span>

## <span data-ttu-id="67869-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67869-135">NOTES</span></span>

## <span data-ttu-id="67869-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67869-136">RELATED LINKS</span></span>

[<span data-ttu-id="67869-137">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="67869-137">Get-AzureRemoteAppVM</span></span>](./Get-AzureRemoteAppVM.md)


