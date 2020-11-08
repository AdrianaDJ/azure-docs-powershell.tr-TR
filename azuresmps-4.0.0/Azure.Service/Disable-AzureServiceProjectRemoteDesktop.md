---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E735FCE5-D82F-42D0-8D74-6A568E55AC17
online version: ''
schema: 2.0.0
ms.openlocfilehash: 433a50a93f8fa8e68021d09d5c1ae464703e227c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105696"
---
# <span data-ttu-id="3f053-101">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="3f053-101">Disable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="3f053-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f053-102">SYNOPSIS</span></span>
<span data-ttu-id="3f053-103">Bulut hizmetine uzak masaüstü erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="3f053-103">Disables Remote Desktop access to a cloud service.</span></span>

## <span data-ttu-id="3f053-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f053-104">SYNTAX</span></span>

```
Disable-AzureServiceProjectRemoteDesktop [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3f053-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f053-105">DESCRIPTION</span></span>
<span data-ttu-id="3f053-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3f053-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3f053-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3f053-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3f053-108">**Disable-AzureServiceProjectRemoteDesktop** , barındırılan bir hizmete uzak masaüstü erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="3f053-108">The **Disable-AzureServiceProjectRemoteDesktop** disables remote desktop access to a hosted service.</span></span>
<span data-ttu-id="3f053-109">Değişikliğin etkinleşmesi için uzak masaüstü erişimi 'ni devre dışı bırakarak hizmeti **Publish-AzureServiceProject** cmdlet 'ini kullanarak yayınlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3f053-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after disabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="3f053-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f053-110">EXAMPLES</span></span>

## <span data-ttu-id="3f053-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f053-111">PARAMETERS</span></span>

### <span data-ttu-id="3f053-112">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3f053-112">-PassThru</span></span>
<span data-ttu-id="3f053-113">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="3f053-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3f053-114">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3f053-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3f053-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="3f053-115">-Profile</span></span>
<span data-ttu-id="3f053-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f053-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3f053-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3f053-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f053-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f053-118">CommonParameters</span></span>
<span data-ttu-id="3f053-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f053-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f053-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f053-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f053-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f053-121">INPUTS</span></span>

## <span data-ttu-id="3f053-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f053-122">OUTPUTS</span></span>

## <span data-ttu-id="3f053-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f053-123">NOTES</span></span>

## <span data-ttu-id="3f053-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f053-124">RELATED LINKS</span></span>

[<span data-ttu-id="3f053-125">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="3f053-125">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)


