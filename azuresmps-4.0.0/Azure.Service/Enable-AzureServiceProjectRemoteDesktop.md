---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 163D2F00-E041-43A9-B077-9034F54B4F3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf258a8f13a344b09f9d5c7119cd78ad202d2ca0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105683"
---
# <span data-ttu-id="2f6a8-101">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="2f6a8-101">Enable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="2f6a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="2f6a8-103">Bir bulut hizmetine uzak masaüstü erişimini mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="2f6a8-103">Enables remote desktop access to a cloud service.</span></span>

## <span data-ttu-id="2f6a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f6a8-104">SYNTAX</span></span>

```
Enable-AzureServiceProjectRemoteDesktop -Username <String> -Password <SecureString> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2f6a8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f6a8-105">DESCRIPTION</span></span>
<span data-ttu-id="2f6a8-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2f6a8-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2f6a8-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2f6a8-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2f6a8-108">**Enable-AzureServiceProjectRemoteDesktop** cmdlet 'i bir bulut hizmetine uzak masaüstü erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="2f6a8-108">The **Enable-AzureServiceProjectRemoteDesktop** cmdlet enables Remote Desktop access to a cloud service.</span></span>
<span data-ttu-id="2f6a8-109">Değişikliğin etkinleşmesi için uzak masaüstü erişimi 'ni etkinleştirdikten sonra, hizmeti **Yayımla-AzureServiceProject** cmdlet 'ini kullanarak yayınlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2f6a8-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after enabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="2f6a8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f6a8-110">EXAMPLES</span></span>

## <span data-ttu-id="2f6a8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f6a8-111">PARAMETERS</span></span>

### <span data-ttu-id="2f6a8-112">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2f6a8-112">-PassThru</span></span>
<span data-ttu-id="2f6a8-113">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="2f6a8-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2f6a8-114">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="2f6a8-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2f6a8-115">-Parola</span><span class="sxs-lookup"><span data-stu-id="2f6a8-115">-Password</span></span>
<span data-ttu-id="2f6a8-116">Parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f6a8-116">Specifies the password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: pwd

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f6a8-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="2f6a8-117">-Profile</span></span>
<span data-ttu-id="2f6a8-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f6a8-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f6a8-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2f6a8-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2f6a8-120">-Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="2f6a8-120">-Username</span></span>
<span data-ttu-id="2f6a8-121">Uzak Masaüstü Protokolü (RDP) aracılığıyla Azure 'daki rol örneğine bağlanırken kullanılacak kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f6a8-121">Specifies the user name to use when connecting to the role instance in Azure via the Remote Desktop Protocol (RDP).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: user

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f6a8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f6a8-122">CommonParameters</span></span>
<span data-ttu-id="2f6a8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f6a8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f6a8-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f6a8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f6a8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f6a8-125">INPUTS</span></span>

## <span data-ttu-id="2f6a8-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f6a8-126">OUTPUTS</span></span>

## <span data-ttu-id="2f6a8-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f6a8-127">NOTES</span></span>

## <span data-ttu-id="2f6a8-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f6a8-128">RELATED LINKS</span></span>

[<span data-ttu-id="2f6a8-129">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="2f6a8-129">Disable-AzureServiceProjectRemoteDesktop</span></span>](./Disable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="2f6a8-130">Yayımla-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="2f6a8-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


